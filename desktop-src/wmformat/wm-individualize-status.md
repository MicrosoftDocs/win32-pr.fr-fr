---
title: Structure WM_INDIVIDUALIZE_STATUS (Drmexternals. h)
description: La \_ \_ structure d’état de l’individualisation WM enregistre l’état du processus d’individualisation.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- Structure WM_INDIVIDUALIZE_STATUS format Windows Media
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb083c2a90a791099f6438f2911ac9735ecd4dada9118811aa0ff581a8db37ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699019"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a>Structure WM_INDIVIDUALIZE_STATUS (Drmexternals. h)

La structure d’état de l' **\_ individualisation \_ WM** enregistre l’état du processus d' [*individualisation*](wmformat-glossary.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a>Membres

<dl> <dt>

**heure(s)**
</dt> <dd>

Code de retour **HRESULT** .

</dd> <dt>

**enIndiStatus**
</dt> <dd>

Valeur du type d’énumération de l’état de l' [**\_ \_ individualisation DRM**](drm-individualization-status.md) .

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère NULL contenant l’URL de réponse d’individualisation.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

**Valeur DWORD** qui indique le nombre d’allers-retours http vers le service d’individualisation qui ont été effectués..

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valeur du type d’énumération de l' [**\_ \_ État http DRM**](drm-http-status.md) .

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

**Valeur DWORD** contenant le nombre d’octets téléchargés jusqu’à présent..

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

**Valeur DWORD** contenant le nombre total d’octets à télécharger. Utilisez cette valeur et **dwHTTPReadProgress** pour afficher une interface utilisateur indiquant la quantité de téléchargement terminée et la quantité restante à effectuer.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est remplie par les composants d’exécution DRM et est envoyée aux applications dans le paramètre *pValue* de la méthode applications [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) lorsque l’événement est égal à WMT \_ Individual. L’application reçoit cet événement plusieurs fois pendant le processus de téléchargement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK ou les versions ultérieures du kit de développement logiciel (SDK)<br/>                       |
| En-tête<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_État http \_ DRM**](drm-http-status.md)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





