# PermissionX

PermissionX是一个用于简化Android运行时权限用法的开源库

添加如下配置将PermissionX引入到你的项目中：

## Setup

```groovy
dependencies {
    ...
    implementation 'com.permissionx.hook:permissionx:1.0.0'
}

## Usage

how to use
```kotlin
PermissionX.request(this,
    android.Manifest.permission.CALL_PHONE){
    allGranted, deniedList ->
       if (allGranted){
           call()
       }else {
           Toast.makeText(this,"You denied $deniedList",Toast.LENGTH_SHORT).show()
       }
    }

```