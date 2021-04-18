---
description: Définit des ID de ressource pour les ressources de type chaîne partagée.
MS-HAID: vspixengine.Resource\_Id
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération Resource_Id
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC04FDC4-CD35-4A87-8EE8-48FFA07B8FC0
api_name:
- Resource_Id
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e7d93111defb01000e32e4f5ade0c9eb09c827e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521892"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span id="vspixengine.resource_id"></span>Énumération de l’ID de ressource \_

Définit des ID de ressource pour les ressources de type chaîne partagée. Celles-ci sont transmises au moteur de capture à partir de l’hôte. Ils sont utilisés pour afficher des chaînes à la superposition HUD de l’application capturée ou pour passer des valeurs de registre des options de Visual Studio à l’Engi de capture.

## <a name="syntax"></a>Syntaxe


```C++
};
```

## <a name="constants"></a>Constantes

<span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**ID \_ ENGINEDISCONNECTED**  
Non utilisé. ID de ressource de la chaîne anciennement utilisé pour indiquer que printscreen a été atteint après la fin de la session de capture.

<span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**\_RCDATA1.**  
Non utilisé.

<span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**\_contenu DEFAULTEXPFILE de l’ID \_**  
Non utilisé. ID de ressource pour la chaîne anciennement utilisée pour les données XML dans les scénarios de capture hérités.

<span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**\_message de capture d’ID \_**  
ID de ressource pour la chaîne « Frame capturé ».

<span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**CAPTURE des ID \_ \_ non \_ prise en charge**  
ID de ressource pour la chaîne « ce programme a indiqué qu’il ne peut pas être utilisé avec les outils de Graphics Diagnostics ».

<span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**titre de capture des ID \_ \_ non \_ pris en charge \_**  
ID de ressource pour la chaîne « fonctionnalités non prises en charge »

<span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**\_fonctionnalité IDS \_ non \_ prise en charge**  
ID de ressource pour la chaîne « niveau de fonctionnalité de l’appareil non pris en charge »

<span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**ID \_ DXVERSION \_ non \_ pris en charge**  
ID de ressource pour la chaîne « version de DirectX non capturable »

<span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**ID \_ DCOMP \_ non \_ pris en charge**  
ID de ressource pour la chaîne « DCOMP en cours d’utilisation par l’application mais non pris en charge sur ce système d’exploitation »

<span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**ID \_ DWRITE \_ non \_ pris en charge**  
ID de ressource pour la chaîne « DWRITE en cours d’utilisation par l’application mais non pris en charge sur ce système d’exploitation »

<span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**\_format d' \_ échec \_ attendu des ID**  
L’ID de ressource de la chaîne « % s » a retourné une erreur lors de la lecture. (HRESULT =% s) \\ r \\ n».

<span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**\_message IDS CAPTURETOOLTIP \_**  
ID de ressource pour la chaîne « utilisez l’écran d’impression » pour capturer une image.»

<span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**ID \_ D2D \_ et \_ D10 \_ non \_ pris en charge**  
ID de ressource pour la chaîne « D2D et D10 non pris en charge ensemble sur ce système d’exploitation »

<span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**\_statistiques HUD \_ ID**  
ID de ressource pour la chaîne "frames capturés% d. Temps de frame (MS)% 0.00 f "

<span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**méthode d’ID \_ interne \_**  
ID de ressource pour la chaîne « méthode interne DirectX »

<span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**\_marque de \_ trame de capture des ID \_**  
ID de ressource pour la chaîne « Frame capturé% LD »

<span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE \_ INPUTASSEMBLER**  
Non utilisé.

<span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE \_ VERTEXSHADER**  
Non utilisé.

<span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE \_ HULLSHADER**  
Non utilisé.

<span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**PIPELINESTAGE \_ TESSELATOR**  
Non utilisé.

<span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE \_ DOMAINSHADER**  
Non utilisé.

<span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE \_ GEOMETRYSHADER**  
Non utilisé.

<span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE \_ STREAMOUTPUT**  
Non utilisé.

<span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**\_RASTÉRISEUR PIPELINESTAGE**  
Non utilisé.

<span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE \_ PIXELSHADER**  
Non utilisé.

<span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE \_ OUTPUTMERGER**  
Non utilisé.

<span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE \_ COMPUTESHADER**  
Non utilisé.

<span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT \_ SUPPORTEDFORMAT**  
Non utilisé.

<span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT \_ CURRENTFORMAT**  
Non utilisé.

<span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**\_en-tête BUFFEROBJECT**  
Non utilisé.

<span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**\_ligne BUFFEROBJECT**  
Non utilisé.

<span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT \_ INVALIDFORMAT**  
Non utilisé.

<span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT \_ INVALIDEMPTYFORMAT**  
Non utilisé.

<span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT \_ INVALIDFORMATSIZE**  
Non utilisé.

<span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO \_ TARGETAPPLICATION**  
Texte affiché dans la fenêtre Propriétés de vsglog-application cible

<span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**SUMMARYINFO \_ chemin d’accès**  
Texte affiché dans le vsglog Fenêtre Propriétés-Path

<span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO \_ TARGETVERSION**  
Texte affiché dans la version vsglog Fenêtre Propriétés-target

<span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO \_ LastModifiedDate &**  
Texte affiché dans le Fenêtre Propriétés vsglog-date de dernière modification

<span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO \_ PROCESSID**  
Texte affiché dans le Fenêtre Propriétés vsglog-ID du processus

<span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO \_ EXPERIMENTFILE**  
Texte affiché dans le fichier vsglog Fenêtre Propriétés-expérimentation

<span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO \_ RUNFILE**  
Texte affiché dans le fichier vsglog Fenêtre Propriétés-Run

<span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**taille de SUMMARYINFO \_**  
Texte affiché dans la taille de Fenêtre Propriétés vsglog

<span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO \_ CREATEDBYPIXVERSION**  
Texte affiché dans le Fenêtre Propriétés vsglog-créé par la version

<span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO \_ SESSIONSTARTTIME**  
Texte affiché dans l’heure de début de la session de Fenêtre Propriétés vsglog

<span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO \_ SYSTEMINFORMATION**  
Texte affiché dans le Fenêtre Propriétés vsglog-informations système

<span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**\_processeur SUMMARYINFO**  
Texte affiché dans le processeur Fenêtre Propriétés vsglog

<span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**\_mémoire SUMMARYINFO**  
Texte affiché dans vsglog Fenêtre Propriétés-Memory

<span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**SUMMARYINFO \_ OSVersion**  
Texte affiché dans la version de vsglog Fenêtre Propriétés-OS

<span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO \_ OSARCHITECTURE**  
Texte affiché dans l’architecture vsglog Fenêtre Propriétés-OS

<span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO \_ TARGETAPPARCHITECTURE**  
Texte affiché dans l’architecture d’application vsglog Fenêtre Propriétés-target

<span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO \_ MAXHWFEATURELEVEL**  
Texte affiché dans le niveau de fonctionnalité matériel de vsglog Fenêtre Propriétés-Max

<span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**SUMMARYINFO \_ DRIVERCONCURRENTCREATES**  
Texte affiché dans le Fenêtre Propriétés vsglog-le pilote crée simultanément

<span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO \_ DRIVERCOMMANDLISTS**  
Texte affiché dans les listes de commandes Fenêtre Propriétés-Driver vsglog

<span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO \_ DOUBLEPRECISIONSHADERS**  
Texte affiché dans les nuanceurs vsglog Fenêtre Propriétés-double précision

<span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO \_ DIRECTCOMPUTECS4X**  
Texte affiché dans le vsglog Fenêtre Propriétés-direct Compute CS 4. x

<span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO \_ 10BITXRHIGHCOLORFORMAT**  
Texte affiché dans le vsglog Fenêtre Propriétés-10BITXRHIGHCOLORFORMAT

<span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO \_ EXTENDEDCOLORFORMATSUPPORT**  
Texte affiché dans le Fenêtre Propriétés vsglog-prise en charge du format de couleur étendu

<span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO \_ DISPLAYINFORMATION**  
Texte affiché dans le Fenêtre Propriétés vsglog-afficher les informations

<span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO \_ DISPLAYNINFORMATION**  
Texte affiché dans le Fenêtre Propriétés vsglog-afficher N informations

<span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**nom de SUMMARYINFO \_**  
Texte affiché dans le nom de Fenêtre Propriétés vsglog

<span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**Description de SUMMARYINFO \_**  
Texte affiché dans le Fenêtre Propriétés vsglog-Description

<span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO \_ DISPLAYMEMORY**  
Texte affiché dans le Fenêtre Propriétés vsglog-afficher la mémoire

<span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO \_ DriverName**  
Texte affiché dans le nom du pilote Fenêtre Propriétés vsglog

<span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO \_ DRIVERVERSION**  
Texte affiché dans la version de vsglog Fenêtre Propriétés-Driver

<span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO \_ MODULEINFORMATION**  
Texte affiché dans les informations du module Fenêtre Propriétés vsglog

<span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO \_ DIRECT3DINFORMATION**  
Texte affiché dans l’vsglog Fenêtre Propriétés-informations Direct3D

<span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO \_ VSGVERSION**  
Texte affiché dans la version de vsglog Fenêtre Propriétés-VSG

<span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO \_ CAPTUREMACHINE**  
Texte affiché dans l’ordinateur de capture Fenêtre Propriétés vsglog

<span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO \_ PLAYBACKMACHINE**  
Texte affiché dans l’ordinateur vsglog Fenêtre Propriétés-playback

<span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**\_REMOTEDATA SUMMARYINFO**  
Texte affiché dans l’vsglog Fenêtre Propriétés-données distantes

<span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO \_ OtherDirect3DInformation**  
Texte affiché dans le Fenêtre Propriétés vsglog-autres informations Direct3D

<span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO \_ SIZEGB**  
Texte affiché dans le Fenêtre Propriétés vsglog-taille Go

<span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO \_ SIZEMB**  
Texte affiché dans le vsglog Fenêtre Propriétés-taille Mo

<span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO \_ SIZEBYTES**  
Texte affiché dans le vsglog Fenêtre Propriétés-octets de taille

<span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO \_ MEMORYMB**  
Texte affiché dans le vsglog Fenêtre Propriétés-Mo de mémoire

<span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO \_ x86**  
Texte affiché dans le Fenêtre Propriétés vsglog-x86

<span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO \_ x64**  
Texte affiché dans le vsglog Fenêtre Propriétés-x64

<span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO \_ true**  
Texte affiché dans le Fenêtre Propriétés vsglog-true

<span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO \_ false**  
Texte affiché dans le Fenêtre Propriétés vsglog-false

<span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO \_ ARM32**  
Texte affiché dans le vsglog Fenêtre Propriétés-ARM 32

<span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO \_ UNKNOWNCPUARCHITECTURE**  
Texte affiché dans le Fenêtre Propriétés vsglog-architecture d’UC inconnue

<span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO \_ AllDXGIFormatValues**  
Texte affiché dans le Fenêtre Propriétés vsglog-toutes les valeurs de format DXGI

<span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO \_ AllD3D11FormatSupportValues**  
Texte affiché dans le Fenêtre Propriétés vsglog-tous les valeurs de prise en charge du format D3D11

<span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**\_ \_ Threads de fonctionnalités SUMMARYINFO d3d11 \_**  
Texte affiché dans le thread de fonctionnalités vsglog Fenêtre Propriétés-D3D11 \_ \_

<span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**SUMMARYINFO \_ DriverConcurrentCreates1**  
Le texte affiché dans le vsglog Fenêtre Propriétés-Driver crée simultanément 1

<span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**SUMMARYINFO \_ DriverCommandLists1**  
Texte affiché dans la commande vsglog Fenêtre Propriétés-Driver Lists 1

<span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**\_ \_ Double fonctionnalité SUMMARYINFO \_ d3d11**  
Texte affiché dans la fonction vsglog Fenêtre Propriétés- \_ d3d11 \_ double

<span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO \_ DoublePrecisionFloatShaderOps**  
Texte affiché dans le vsglog Fenêtre Propriétés-double précision opérations de nuanceur float

<span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO \_ d3d11 \_ fonctionnalité \_ D3D10 \_ X \_ options matérielles \_**  
Texte affiché dans le vsglog Fenêtre Propriétés-D3D11 \_ fonctionnalité \_ \_ \_ options matérielles D3D10 X \_

<span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO \_ ComputeShaders \_ plus \_ RawAndStructuredBuffers \_ via \_ Shader \_ 4 \_ x**  
Texte affiché dans vsglog Fenêtre Propriétés-ComputeShaders + RAW et structure dBuffers via le Shader 4. x

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**\_ \_ \_ Options d3d11 de la fonctionnalité d3d11 SUMMARYINFO \_**  
Texte affiché dans les \_ \_ options de d3d11 de vsglog fenêtre Propriétés-d3d11 \_

<span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**SUMMARYINFO \_ OutputMergerLogicOp**  
Texte affiché dans la logique de fusion vsglog Fenêtre Propriétés-output

<span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO \_ UAVOnlyRenderingForcedSampleCount**  
Texte affiché dans le nombre d’échantillons forcés du rendu vsglog Fenêtre Propriétés-UAV uniquement

<span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO \_ DiscardAPIsSeenByDriver**  
Texte affiché dans les API vsglog Fenêtre Propriétés-ignore détectées par le pilote

<span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**SUMMARYINFO \_ FlagsForUpdateAndCopySeenByDriver**  
Texte affiché dans les indicateurs de Fenêtre Propriétés vsglog pour la mise à jour et la copie détectée par le pilote

<span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO \_ Clearview**  
Texte affiché dans le Fenêtre Propriétés vsglog-Clear View

<span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO \_ CopyWithOverlap**  
Texte affiché dans le Fenêtre Propriétés vsglog-copy with chevauchement

<span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO \_ ConstantBufferPartialUpdate**  
Texte affiché dans la mise à jour partielle du tampon vsglog Fenêtre Propriétés-constant

<span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO \_ ConstantBufferOffsetting**  
Texte affiché dans le vsglog Fenêtre Propriétés-décalage de la mémoire tampon constante

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicConstantBuffer**  
Texte affiché dans le Fenêtre Propriétés vsglog-Map ne pas remplacer sur une mémoire tampon constante dynamique

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicBufferSRV**  
Texte affiché dans le Fenêtre Propriétés vsglog-Map ne pas remplacer sur le tampon dynamique SRV

<span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO \_ MultisampleRTVWithForcedSampleCountOne**  
Texte affiché dans l’vsglog Fenêtre Propriétés-exemple RTV avec un échantillon forcé nombre un

<span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ SAD4ShaderInstructions**  
Texte affiché dans les instructions du nuanceur vsglog Fenêtre Propriétés-SAD4

<span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ ExtendedDoublesShaderInstructions**  
Texte affiché dans le Fenêtre Propriétés vsglog-instructions du nuanceur double étendu

<span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO \_ ExtendedResourceSharing**  
Texte affiché dans le Fenêtre Propriétés vsglog-partage de ressources étendu

<span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**\_ \_ \_ Informations sur l’architecture des fonctionnalités SUMMARYINFO d3d11 \_**  
Texte affiché dans les informations sur l’architecture de la fonctionnalité vsglog Fenêtre Propriétés-D3D11 \_ \_ \_

<span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO \_ TileBasedDeferredRenderer**  
Texte affiché dans le convertisseur différé basé sur des mosaïques Fenêtre Propriétés vsglog

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**\_ \_ \_ Options d3d9 de la fonctionnalité d3d11 SUMMARYINFO \_**  
Texte affiché dans les \_ \_ options de d3d9 de vsglog fenêtre Propriétés-d3d11 \_

<span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO \_ FullNonPow2TextureSupport**  
Texte affiché dans le Fenêtre Propriétés vsglog-prise en charge complète de la texture non-Pow2

<span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**\_ \_ \_ \_ \_ Prise en charge de la précision minimale du nuanceur de fonctionnalités SUMMARYINFO d3d11 \_**  
Texte affiché dans la fonctionnalité vsglog Fenêtre Propriétés-D3D11, \_ \_ \_ \_ \_ prise en charge de la précision minimale du nuanceur

<span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO \_ PixelShaderMinPrecision**  
Texte affiché dans le nuanceur de vsglog Fenêtre Propriétés-pixel-précision min.

<span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO \_ AllOtherShaderStagesMinPrecision**  
Texte affiché dans le Fenêtre Propriétés vsglog-tous les autres niveaux de nuanceur min précision

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**SUMMARYINFO \_ d3d11 \_ fonctionnalité \_ d3d9 \_ Shadow \_ support**  
Texte affiché dans la fonctionnalité vsglog Fenêtre Propriétés- \_ d3d11 \_ \_ \_ prise en charge des Shadows d3d9

<span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO \_ SupportsDepthAsTextureWithLessEqualComparisonFilter**  
Texte affiché dans le Fenêtre Propriétés vsglog-prend en charge la profondeur comme texture avec un filtre de comparaison moins égal

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO \_ d3d11 \_ fonctionnalité \_ d3d11 \_ options1**  
Texte affiché dans la fonctionnalité vsglog Fenêtre Propriétés- \_ d3d11 \_ d3d11 \_ options1

<span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO \_ TiledResourcesTier**  
Texte affiché dans le niveau des ressources en mosaïque Fenêtre Propriétés vsglog

<span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO \_ MinMaxFiltering**  
Texte affiché dans le vsglog Fenêtre Propriétés-min max Filtering

<span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO \_ ClearViewAlsoSupportsDepthOnlyFormats**  
Le texte affiché dans vsglog Fenêtre Propriétés-Clear View prend également en charge les formats de profondeur uniquement

<span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO \_ MapOnDefaultBuffers**  
Texte affiché dans le Fenêtre Propriétés vsglog-Map sur les mémoires tampons par défaut

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**SUMMARYINFO \_ d3d11 \_ fonctionnalité \_ d3d9 \_ la \_ \_ prise en charge de l’instanciation simple**  
Texte affiché dans la fonctionnalité vsglog Fenêtre Propriétés- \_ d3d11 \_ d3d9 \_ \_ \_ prise en charge de l’instanciation simple

<span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO \_ SimpleInstancingSupported0**  
Texte affiché dans le vsglog Fenêtre Propriétés-instance simple prise en charge 0

<span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**\_ \_ \_ Prise en charge des marqueurs de fonctionnalités SUMMARYINFO d3d11 \_**  
Texte affiché dans la \_ \_ \_ prise en charge des marqueurs de fonctionnalité VSGLOG fenêtre Propriétés-d3d11

<span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**\_Profil SUMMARYINFO**  
Texte affiché dans le profil Fenêtre Propriétés vsglog

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO \_ d3d11 \_ fonctionnalité \_ d3d9 \_ options1**  
Texte affiché dans la fonctionnalité vsglog Fenêtre Propriétés- \_ d3d11 \_ d3d9 \_ options1

<span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO \_ FullNonPow2TextureSupported**  
Texte affiché dans le Fenêtre Propriétés vsglog-texture complète non Pow2 prise en charge

<span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO \_ DepthAsTextureWithLessEqualComparisonFilterSupported**  
Texte affiché dans le Fenêtre Propriétés vsglog-profondeur comme texture avec un filtre de comparaison moins égal pris en charge

<span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO \_ SimpleInstancingSupported1**  
Texte affiché dans vsglog Fenêtre Propriétés-instance simple prise en charge 1

<span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO \_ TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**  
Texte affiché dans la cible de rendu de la face de cube Fenêtre Propriétés-texture vsglog avec le stencil de profondeur non cube pris en charge

<span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO \_ DXGIFormat**  
Texte affiché dans le vsglog Fenêtre Propriétés-DXGIFormat

<span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO \_ DXGIFormat1**  
Texte affiché dans le vsglog Fenêtre Propriétés-DXGIFormat1

<span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**SUMMARYINFO \_ MODULENAME**  
Texte affiché dans le vsglog Fenêtre Propriétés-MODULENAME

<span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**CONFIGURATION d’IDD \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu dans VsGraphicsRemoteEngine

<span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**\_icône d' \_ en-tête statique IDC \_**  
Texte affiché dans l’icône de contrôle de boîte de dialogue Configurer le pare-feu-en-tête statique

<span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**\_ \_ en-tête statique IDC**  
Texte affiché dans le contrôle de boîte de dialogue Configurer le pare-feu-en-tête statique

<span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**\_configuration de \_ pare-feu statique IDC \_**  
Texte affiché dans le contrôle configurer la boîte de dialogue pare-feu-configuration de pare-feu statique

<span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**\_icône de \_ FW \_ statique IDC**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-icône de pare-feu statique

<span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**\_ \_ en-tête de FW statique IDC \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-en-tête de pare-feu statique

<span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**\_pare- \_ feu de GroupBox STATIQUEs IDC \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-pare-feu GroupBox statique

<span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC \_ vérification \_ des \_ réseaux de domaine FW \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-vérifier les réseaux de domaine de pare-feu

<span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC \_ vérification \_ des \_ réseaux privés de FW \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-vérifier les réseaux privés du pare-feu

<span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC \_ vérification \_ des \_ réseaux publics du FW \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-vérifier les réseaux publics de pare-feu

<span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**\_configuration du bouton IDC \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-bouton de commande configurer

<span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**annulation de la configuration de l’ID \_ \_**  
Texte affiché dans le contrôle de boîte de dialogue Configurer le pare-feu-annuler la configuration

<span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**IDENTIFICATEURs de \_ texte du \_ firmware \_ non \_ configuré**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-texte pare-feu non configuré

<span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**ID du texte des ID \_ \_ \_ configuré**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-texte configuré

<span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**nom de la \_ règle de pare-feu IDS \_ \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-nom de la règle de pare-feu

<span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**Description de la \_ règle de pare-feu IDS \_ \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-Description de la règle de pare-feu

<span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**\_ \_ en-tête statique IDS**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-en-tête statique

<span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**nom de la configuration des ID \_ \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-nom de la configuration

<span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**\_ \_ en-tête de FW statique des ID \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-en-tête de pare-feu statique

<span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**\_FW de \_ GroupBox \_ statique de l’ID**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-pare-feu de zone statique

<span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**ID \_ vérification \_ des \_ réseaux de domaine du FW \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-vérifier les réseaux de domaine de pare-feu

<span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**ID \_ vérifier \_ les \_ réseaux privés du FW \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-vérifier les réseaux privés du pare-feu

<span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**ID \_ vérification \_ des \_ réseaux publics du FW \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-vérifier les réseaux publics de pare-feu

<span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**\_bouton ID \_ configurer**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-buttom confiture

<span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**annulation de la configuration des ID \_ \_**  
Texte affiché dans la boîte de dialogue Configurer le pare-feu-annulation de la configuration

<span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**ID \_ CAPTURETOOLTIP \_ message \_ CORESYSTEM**  
ID de ressource pour la chaîne « utilisez le bouton capturer dans Visual Studio pour capturer le ou les frames ».

<span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**ID \_ et \_ aucun**  
Non utilisé.

<span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**ID \_ et \_ SESSIONSTART**  
Non utilisé.

<span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**ID \_ et \_ SESSIONEND**  
Non utilisé.

<span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**ID \_ et \_ PROCESSSTART**  
Non utilisé.

<span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**ID \_ et \_ PROCESSEND**  
Non utilisé.

<span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**ID \_ et \_ FRAMEBEGIN**  
Non utilisé.

<span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**ID \_ et \_ FRAMEEND**  
Non utilisé.

<span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**ID \_ et \_ USEREVENTBEGIN**  
Non utilisé.

<span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**ID \_ et \_ USEREVENTEND**  
Non utilisé.

<span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**ID \_ et \_ USERMARKER**  
Non utilisé.

<span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**ID \_ et \_ appel**  
Non utilisé.

<span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**ID \_ et \_ OBJECTPOPULATION**  
Non utilisé.

<span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**ID \_ et \_ OBJECTCREATION**  
Non utilisé.

<span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**ID \_ et \_ CALLSYNC**  
Non utilisé.

<span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**ID \_ et \_ inconnu**  
Non utilisé.

<span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**\_déclencheur IDS \_ None**  
Non utilisé.

<span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**\_déclencheur IDS \_ PROGRAMSTART**  
Non utilisé.

<span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**\_Frame de déclencheur IDS \_**  
Non utilisé.

<span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**\_heure du déclenchement des ID \_**  
Non utilisé.

<span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**\_déclencheur IDS \_ USERMARKER**  
Non utilisé.

<span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**\_déclencheur IDS \_ BEGINUSEREVENT**  
Non utilisé.

<span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**\_déclencheur IDS \_ ENDUSEREVENT**  
Non utilisé.

<span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**\_déclencheur IDS \_ CAPTUREFRAME**  
Non utilisé.

<span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**\_déclencheur IDS \_ APICAPTURE**  
Non utilisé.

<span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**ID d' \_ erreur \_ CALLDATA**  
Non utilisé.

<span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**ID d' \_ erreur \_ CREATINGLOG**  
Non utilisé.

<span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**ID \_ UNKNOWNCALL**  
Non utilisé.

<span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**niveau de fonctionnalité d’avertissement des ID \_ \_ \_ \_ modifié**  
Non utilisé.

<span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**\_fréquence d’état de l’ID \_**  

<span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID de \_ désactivation du \_ HUD**  

<span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**compatibilité des ID de \_ désactivation \_**  

<span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID de \_ collecte \_ piles**  

<span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**ID \_ Enable \_ SDKERROR \_ Stop**  

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



