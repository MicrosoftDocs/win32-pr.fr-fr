---
title: Structure MPSIGUPDATE_DATA (MpClient. h)
description: Données de notification transmises à la fonction de rappel de mise à jour de signature.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- fonctionnalités d’environnement Windows héritées de la structure MPSIGUPDATE_DATA
- PMPSIGUPDATE_DATA des fonctionnalités d’environnement du pointeur de structure Windows hérité
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3c117b92882a24a825aee5c5b008e10721c40b8a93d26a9a677bb79858635c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476251"
---
# <a name="mpsigupdate_data-structure"></a>\_Structure de données MPSIGUPDATE

Données de notification transmises à la fonction de rappel de mise à jour de signature.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwPercentComplete**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Une estimation du pourcentage pour toutes les mises à jour qui ont été téléchargées et/ou installées.

</dd> <dt>

**dwTotalUpdates**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Nombre total de mises à jour à télécharger et/ou à installer.

</dd> <dt>

**dwCurrentUpdateIndex**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Valeur d’index de base zéro qui spécifie quelle mise à jour parmi celles requises est actuellement en cours de téléchargement et/ou d’installation.

</dd> <dt>

**eType**
</dt> <dd>

Type : **MPSIGUPDATE \_**

</dd> <dd>

Type de mise à jour. Une des valeurs possibles suivantes :



| Valeur                                                                                                                                                                                                                             | Signification                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**MPSIGUPDATE \_ type \_ None**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**\_type MPSIGUPDATE \_ géré**</dt> </dl>                                   | Mise à jour WSUS. L’annulation nécessite des droits d’administrateur.<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**\_type MPSIGUPDATE \_ http**</dt> </dl>                                            | Mise à jour HTTP. Droits d’administrateur non nécessaires pour annuler.<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**\_type MPSIGUPDATE \_ http \_ SRV**</dt> </dl>                               | HTTP à partir du service. L’annulation nécessite des droits d’administrateur.<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**MPSIGUPDATE \_ type \_ UNC**</dt> </dl>                                               | Partage UNC. Droits d’administrateur non nécessaires pour annuler.<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**\_type MPSIGUPDATE \_ non géré**</dt> </dl>                             | Mise à jour MU/WU. L’annulation nécessite des droits d’administrateur.<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**\_ \_ plateforme managée de type MPSIGUPDATE \_**</dt> </dl>       | Mise à jour WSUS pour la plateforme. L’annulation nécessite des droits d’administrateur.<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**\_ \_ plateforme non managée de type MPSIGUPDATE \_**</dt> </dl> | Mise à jour de MU/WU pour la plateforme. L’annulation nécessite des droits d’administrateur.<br/> |



 

</dd> <dt>

**Étape**
</dt> <dd>

Type : **\_ \_ phase de mise à jour du pack d’installation**

</dd> <dd>

Étape de mise à jour. Une des valeurs possibles suivantes :



| Valeur                                                                                                                                                                         | Signification                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**étape de point de gestion \_ \_ inconnue**</dt> </dl>       | Étape de mise à jour inconnue.<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**\_ \_ mise à jour de recherche de Pack d’e**</dt> </dl>       | Étape de recherche de mise à jour.<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**\_ \_ mise à jour du téléchargement du pack d’e**</dt> </dl> | Étape de téléchargement de la mise à jour.<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**\_ \_ mise à jour d’installation du pack d’installation**</dt> </dl>    | Mettez à jour l’étape d’installation.<br/>  |



 

</dd> <dt>

**Chemin d’accès**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Mettre à jour le chemin.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





