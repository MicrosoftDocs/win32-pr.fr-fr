---
title: Structure WM_GET_LICENSE_DATA (Drmexternals. h)
description: La \_ structure de données de licence de l’obtention de la licence WM contient des \_ \_ informations sur l’emplacement d’acquisition d’une licence DRM.
ms.assetid: 7e8053d5-f3f5-4519-97f5-6dbd89982f3a
keywords:
- Structure WM_GET_LICENSE_DATA format Windows Media
topic_type:
- apiref
api_name:
- WM_GET_LICENSE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f53b6ddfd532710e712637c57785d8893d8f977807bfb45cac0fc787ccbf58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844473"
---
# <a name="wm_get_license_data-structure"></a>WM- \_ recevoir la structure des \_ données de licence \_

La structure de données de licence de l’obtention de la **\_ \_ licence \_ WM** contient des informations sur l’emplacement d’acquisition d’une [*licence*](wmformat-glossary.md) [*DRM*](wmformat-glossary.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WMGetLicenseData {
  DWORD   dwSize;
  HRESULT hr;
  WCHAR   *wszURL;
  WCHAR   *wszLocalFilename;
  BYTE    *pbPostData;
  DWORD   dwPostDataSize;
} WM_GET_LICENSE_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSize nul**
</dt> <dd>

**Valeur DWORD** contenant la taille de la structure de données de la **\_ \_ licence \_ WM** , en octets.

</dd> <dt>

**heure(s)**
</dt> <dd>

Code de retour **HRESULT** .

</dd> <dt>

**wszURL**
</dt> <dd>

Chaîne de caractères larges se terminant par un caractère NULL contenant l’URL d’acquisition de licence. Utilisez cette chaîne et la chaîne **pbPostData** dans l’acquisition de licence non silencieuse.

</dd> <dt>

**wszLocalFilename**
</dt> <dd>

Chaîne de caractères larges se terminant par un caractère null qui contient une page HTML locale générée par le composant DRM. Lorsque cette chaîne est chargée dans un navigateur, elle redirige automatiquement la requête HTTP vers l’URL d’acquisition de licence, ainsi que les données de publication nécessaires. L’utilisation de cette URL locale est désormais déconseillée. L’approche recommandée consiste à utiliser les chaînes **wszURL** et **pbPostData** .

</dd> <dt>

**pbPostData**
</dt> <dd>

Pointeur vers un tableau d’octets contenant les données à publier dans l’URL d’acquisition de licence. Vous devez ajouter la chaîne suivante au début de la chaîne **pbPostData** : « unsilent = 1&Challenge = ». La chaîne résultante doit ensuite être ajoutée à **wszURL** lorsque vous formez la requête http.

</dd> <dt>

**dwPostDataSize**
</dt> <dd>

**Valeur DWORD** qui indique la taille de **pbPostData** sans la chaîne « non Silent = 1&Challenge = » référencée dans **pbPostData**.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure remplie est retournée dans le paramètre *pValue* de la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) si l' **\_ État WMT** est égal à **WMT, \_ aucun \_ droit \_ n'** a été acquis par le biais d’une **\_ \_ licence** WMT. Pour le service WMT \_ \_ , aucun droit \_ ex Events, le membre **HR** est une \_ licence NS e \_ \_ Required, NS \_ e \_ License \_ obsolète ou NS \_ e \_ License \_ incorrect \_ Rights. L’une de ces erreurs indique qu’une nouvelle licence doit être acquise en accédant à l’URL dans le membre **wszURL** .

Pour les \_ événements d’acquisition de \_ licence WMT, le membre **RH** passera la macro SUCCEEDED si une licence a été acquise avec succès. Si cet événement est reçu après une tentative d’acquisition en mode silencieux et que l' **heure** d’été est égale à \_ \_ \_ la NOTACQUIRED de licence NS E DRM \_ , cela signifie que seule l’acquisition non silencieuse est prise en charge par le serveur de licences pour cette licence.

L’exemple d’application audioplayer montre comment utiliser correctement les informations retournées dans cette structure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK ou les versions ultérieures du kit de développement logiciel (SDK)<br/>                       |
| En-tête<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMDRMReader :: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





