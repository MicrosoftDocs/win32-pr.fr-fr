---
title: Structure WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)
description: La \_ structure d’état de l’individualisation WM \_ contient des informations sur un processus d’individualisation en attente.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- Structure WM_INDIVIDUALIZE_STATUS format Windows Media
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295187"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>Structure WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)

La structure d’état de l' **\_ \_ individualisation WM** contient des informations sur un processus d’individualisation en attente.

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

Valeur du type d’énumération de l’état de l' [**\_ \_ individualisation DRM**](drmdrm-individualization-status.md) qui indique l’état actuel du processus d’individualisation.

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère NULL contenant l’URL de réponse d’individualisation.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

Nombre d’allers-retours HTTP vers le service d’individualisation qui ont été effectués.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valeur du type d’énumération de l' [**\_ \_ État http DRM**](drmdrm-http-status.md) .

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

Nombre d’octets téléchargés.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

Nombre total d’octets à télécharger. Vous pouvez utiliser cette valeur et **dwHTTPReadProgress** pour afficher une interface utilisateur indiquant la quantité de téléchargement terminée et la quantité restante à effectuer.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est reçue lorsque vous appelez la méthode [**IWMDRMIndividualizationStatus :: GetStatus**](iwmdrmindividualizationstatus-getstatus.md) . Elle contient l’état du processus d’individualisation en attente au moment de l’appel.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





