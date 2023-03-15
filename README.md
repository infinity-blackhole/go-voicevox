# Go API client for voicevox

VOICEVOXの音声合成エンジンです。

## Overview
This API client was generated by the [OpenAPI Generator](https://openapi-generator.tech) project.  By using the [OpenAPI-spec](https://www.openapis.org/) from a remote server, you can easily generate an API client.

- API version: latest
- Package version: 1.0.0
- Build package: org.openapitools.codegen.languages.GoClientCodegen

## Installation

Install the following dependencies:

```shell
go get github.com/stretchr/testify/assert
go get golang.org/x/net/context
```

Put the package under your project folder and add the following in import:

```golang
import voicevox "github/infinity-blackhole/go-voicevox"
```

To use a proxy, set the environment variable `HTTP_PROXY`:

```golang
os.Setenv("HTTP_PROXY", "http://proxy_name:proxy_port")
```

## Configuration of Server URL

Default configuration comes with `Servers` field that contains server objects as defined in the OpenAPI specification.

### Select Server Configuration

For using other server than the one defined on index 0 set context value `sw.ContextServerIndex` of type `int`.

```golang
ctx := context.WithValue(context.Background(), voicevox.ContextServerIndex, 1)
```

### Templated Server URL

Templated server URL is formatted using default variables from configuration or from context value `sw.ContextServerVariables` of type `map[string]string`.

```golang
ctx := context.WithValue(context.Background(), voicevox.ContextServerVariables, map[string]string{
	"basePath": "v2",
})
```

Note, enum values are always validated and all unused variables are silently ignored.

### URLs Configuration per Operation

Each operation can use different server URL defined using `OperationServers` map in the `Configuration`.
An operation is uniquely identified by `"{classname}Service.{nickname}"` string.
Similar rules for overriding default operation server index and variables applies by using `sw.ContextOperationServerIndices` and `sw.ContextOperationServerVariables` context maps.

```golang
ctx := context.WithValue(context.Background(), voicevox.ContextOperationServerIndices, map[string]int{
	"{classname}Service.{nickname}": 2,
})
ctx = context.WithValue(context.Background(), voicevox.ContextOperationServerVariables, map[string]map[string]string{
	"{classname}Service.{nickname}": {
		"port": "8443",
	},
})
```

## Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**AccentPhrasesAccentPhrasesPost**](docs/DefaultApi.md#accentphrasesaccentphrasespost) | **Post** /accent_phrases | テキストからアクセント句を得る
*DefaultApi* | [**AddPresetAddPresetPost**](docs/DefaultApi.md#addpresetaddpresetpost) | **Post** /add_preset | Add Preset
*DefaultApi* | [**AddUserDictWordUserDictWordPost**](docs/DefaultApi.md#adduserdictworduserdictwordpost) | **Post** /user_dict_word | Add User Dict Word
*DefaultApi* | [**AudioQueryAudioQueryPost**](docs/DefaultApi.md#audioqueryaudioquerypost) | **Post** /audio_query | 音声合成用のクエリを作成する
*DefaultApi* | [**AudioQueryFromPresetAudioQueryFromPresetPost**](docs/DefaultApi.md#audioqueryfrompresetaudioqueryfrompresetpost) | **Post** /audio_query_from_preset | 音声合成用のクエリをプリセットを用いて作成する
*DefaultApi* | [**CancellableSynthesisCancellableSynthesisPost**](docs/DefaultApi.md#cancellablesynthesiscancellablesynthesispost) | **Post** /cancellable_synthesis | 音声合成する（キャンセル可能）
*DefaultApi* | [**ConnectWavesConnectWavesPost**](docs/DefaultApi.md#connectwavesconnectwavespost) | **Post** /connect_waves | base64エンコードされた複数のwavデータを一つに結合する
*DefaultApi* | [**CoreVersionsCoreVersionsGet**](docs/DefaultApi.md#coreversionscoreversionsget) | **Get** /core_versions | Core Versions
*DefaultApi* | [**DeletePresetDeletePresetPost**](docs/DefaultApi.md#deletepresetdeletepresetpost) | **Post** /delete_preset | Delete Preset
*DefaultApi* | [**DeleteUserDictWordUserDictWordWordUuidDelete**](docs/DefaultApi.md#deleteuserdictworduserdictwordworduuiddelete) | **Delete** /user_dict_word/{word_uuid} | Delete User Dict Word
*DefaultApi* | [**DownloadableLibrariesDownloadableLibrariesGet**](docs/DefaultApi.md#downloadablelibrariesdownloadablelibrariesget) | **Get** /downloadable_libraries | Downloadable Libraries
*DefaultApi* | [**EngineManifestEngineManifestGet**](docs/DefaultApi.md#enginemanifestenginemanifestget) | **Get** /engine_manifest | Engine Manifest
*DefaultApi* | [**GetPresetsPresetsGet**](docs/DefaultApi.md#getpresetspresetsget) | **Get** /presets | Get Presets
*DefaultApi* | [**GetUserDictWordsUserDictGet**](docs/DefaultApi.md#getuserdictwordsuserdictget) | **Get** /user_dict | Get User Dict Words
*DefaultApi* | [**ImportUserDictWordsImportUserDictPost**](docs/DefaultApi.md#importuserdictwordsimportuserdictpost) | **Post** /import_user_dict | Import User Dict Words
*DefaultApi* | [**InitializeSpeakerInitializeSpeakerPost**](docs/DefaultApi.md#initializespeakerinitializespeakerpost) | **Post** /initialize_speaker | Initialize Speaker
*DefaultApi* | [**InstallLibraryInstallLibraryLibraryUuidPost**](docs/DefaultApi.md#installlibraryinstalllibrarylibraryuuidpost) | **Post** /install_library/{library_uuid} | Install Library
*DefaultApi* | [**InstalledLibrariesInstalledLibrariesGet**](docs/DefaultApi.md#installedlibrariesinstalledlibrariesget) | **Get** /installed_libraries | Installed Libraries
*DefaultApi* | [**IsInitializedSpeakerIsInitializedSpeakerGet**](docs/DefaultApi.md#isinitializedspeakerisinitializedspeakerget) | **Get** /is_initialized_speaker | Is Initialized Speaker
*DefaultApi* | [**MoraDataMoraDataPost**](docs/DefaultApi.md#moradatamoradatapost) | **Post** /mora_data | アクセント句から音高・音素長を得る
*DefaultApi* | [**MoraLengthMoraLengthPost**](docs/DefaultApi.md#moralengthmoralengthpost) | **Post** /mora_length | アクセント句から音素長を得る
*DefaultApi* | [**MoraPitchMoraPitchPost**](docs/DefaultApi.md#morapitchmorapitchpost) | **Post** /mora_pitch | アクセント句から音高を得る
*DefaultApi* | [**MorphableTargetsMorphableTargetsPost**](docs/DefaultApi.md#morphabletargetsmorphabletargetspost) | **Post** /morphable_targets | 指定した話者に対してエンジン内の話者がモーフィングが可能か判定する
*DefaultApi* | [**MultiSynthesisMultiSynthesisPost**](docs/DefaultApi.md#multisynthesismultisynthesispost) | **Post** /multi_synthesis | 複数まとめて音声合成する
*DefaultApi* | [**RewriteUserDictWordUserDictWordWordUuidPut**](docs/DefaultApi.md#rewriteuserdictworduserdictwordworduuidput) | **Put** /user_dict_word/{word_uuid} | Rewrite User Dict Word
*DefaultApi* | [**SettingGetSettingGet**](docs/DefaultApi.md#settinggetsettingget) | **Get** /setting | Setting Get
*DefaultApi* | [**SettingPostSettingPost**](docs/DefaultApi.md#settingpostsettingpost) | **Post** /setting | Setting Post
*DefaultApi* | [**SpeakerInfoSpeakerInfoGet**](docs/DefaultApi.md#speakerinfospeakerinfoget) | **Get** /speaker_info | Speaker Info
*DefaultApi* | [**SpeakersSpeakersGet**](docs/DefaultApi.md#speakersspeakersget) | **Get** /speakers | Speakers
*DefaultApi* | [**SupportedDevicesSupportedDevicesGet**](docs/DefaultApi.md#supporteddevicessupporteddevicesget) | **Get** /supported_devices | Supported Devices
*DefaultApi* | [**SynthesisMorphingSynthesisMorphingPost**](docs/DefaultApi.md#synthesismorphingsynthesismorphingpost) | **Post** /synthesis_morphing | 2人の話者でモーフィングした音声を合成する
*DefaultApi* | [**SynthesisSynthesisPost**](docs/DefaultApi.md#synthesissynthesispost) | **Post** /synthesis | 音声合成する
*DefaultApi* | [**UpdatePresetUpdatePresetPost**](docs/DefaultApi.md#updatepresetupdatepresetpost) | **Post** /update_preset | Update Preset
*DefaultApi* | [**VersionVersionGet**](docs/DefaultApi.md#versionversionget) | **Get** /version | Version


## Documentation For Models

 - [AccentPhrase](docs/AccentPhrase.md)
 - [AccentPhrasePauseMora](docs/AccentPhrasePauseMora.md)
 - [AudioQuery](docs/AudioQuery.md)
 - [DownloadableLibrary](docs/DownloadableLibrary.md)
 - [EngineManifest](docs/EngineManifest.md)
 - [EngineManifestSupportedFeatures](docs/EngineManifestSupportedFeatures.md)
 - [HTTPValidationError](docs/HTTPValidationError.md)
 - [LibrarySpeaker](docs/LibrarySpeaker.md)
 - [LibrarySpeakerSpeaker](docs/LibrarySpeakerSpeaker.md)
 - [LibrarySpeakerSpeakerInfo](docs/LibrarySpeakerSpeakerInfo.md)
 - [LicenseInfo](docs/LicenseInfo.md)
 - [Mora](docs/Mora.md)
 - [MorphableTargetInfo](docs/MorphableTargetInfo.md)
 - [ParseKanaBadRequest](docs/ParseKanaBadRequest.md)
 - [Preset](docs/Preset.md)
 - [Speaker](docs/Speaker.md)
 - [SpeakerInfo](docs/SpeakerInfo.md)
 - [SpeakerStyle](docs/SpeakerStyle.md)
 - [SpeakerSupportPermittedSynthesisMorphing](docs/SpeakerSupportPermittedSynthesisMorphing.md)
 - [SpeakerSupportedFeatures](docs/SpeakerSupportedFeatures.md)
 - [StyleInfo](docs/StyleInfo.md)
 - [SupportedDevicesInfo](docs/SupportedDevicesInfo.md)
 - [SupportedFeatures](docs/SupportedFeatures.md)
 - [UpdateInfo](docs/UpdateInfo.md)
 - [UserDictWord](docs/UserDictWord.md)
 - [ValidationError](docs/ValidationError.md)
 - [WordTypes](docs/WordTypes.md)


## Documentation For Authorization

 Endpoints do not require authorization.


## Documentation for Utility Methods

Due to the fact that model structure members are all pointers, this package contains
a number of utility functions to easily obtain pointers to values of basic types.
Each of these functions takes a value of the given basic type and returns a pointer to it:

* `PtrBool`
* `PtrInt`
* `PtrInt32`
* `PtrInt64`
* `PtrFloat`
* `PtrFloat32`
* `PtrFloat64`
* `PtrString`
* `PtrTime`

## Author



