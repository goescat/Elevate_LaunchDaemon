# Elevate_LaunchDaemon

放到 `/Library/LaunchDaemons`

```
sudo launchctl bootstrap system /Library/LaunchDaemons/com.example.jamf.policy.plist
```

### 其他指令
#### 結束
```
sudo launchctl bootout system/com.example.jamf.policy.plist
```

#### 驗證 plist
```
plutil -lint /Library/LaunchDaemons/com.example.jamf.policy.plist
```

#### 檢查狀態
```
sudo launchctl print system/com.example.jamf.policy.plist
```

#### 不等排程立即執行一次
```
sudo launchctl kickstart -k system/com.example.jamf.policy.plist
```
