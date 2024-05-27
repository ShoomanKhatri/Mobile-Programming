{
  "name": "Android Development",
  "image": "mcr.microsoft.com/vscode/devcontainers/base:ubuntu",
  "features": {
    "ghcr.io/devcontainers/features/java:1": {
      "version": "11"
    }
  },
  "postCreateCommand": "sudo apt update && sudo apt install -y wget unzip openjdk-11-jdk && mkdir -p /usr/local/android-sdk/cmdline-tools && wget https://dl.google.com/android/repository/commandlinetools-linux-7583922_latest.zip -O /usr/local/android-sdk/cmdline-tools.zip && unzip /usr/local/android-sdk/cmdline-tools.zip -d /usr/local/android-sdk/cmdline-tools && mv /usr/local/android-sdk/cmdline-tools/cmdline-tools /usr/local/android-sdk/cmdline-tools/latest && yes | /usr/local/android-sdk/cmdline-tools/latest/bin/sdkmanager --licenses && /usr/local/android-sdk/cmdline-tools/latest/bin/sdkmanager --install 'platforms;android-30' 'build-tools;30.0.3' 'system-images;android-30;google_apis;x86_64' 'emulator' 'platform-tools'",
  "postStartCommand": "touch ~/.bashrc && echo 'export ANDROID_HOME=/usr/local/android-sdk' >> ~/.bashrc && echo 'export PATH=$ANDROID_HOME/cmdline-tools/latest/bin:$ANDROID_HOME/platform-tools:$PATH' >> ~/.bashrc && source ~/.bashrc",
  "customizations": {
    "vscode": {
      "extensions": [
        "ms-vscode.vscode-typescript-next",
        "vscjava.vscode-java-pack",
        "ms-azuretools.vscode-docker",
        "ms-vscode-remote.remote-containers",
        "ms-androidtools.android-emulator"
      ]
    }
  },
  "mounts": [
    "source=/dev/kvm,target=/dev/kvm,type=bind"
  ]
}
