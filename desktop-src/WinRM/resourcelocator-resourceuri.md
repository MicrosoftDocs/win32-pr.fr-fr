---
title: Propriété ResourceLocator. ResourceURI (WSManDisp. h)
description: Obtient ou définit l’URI de ressource dans un objet ResourceLocator.
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- Propriété ResourceURI Windows Remote Management
- Propriété ResourceURI Windows Remote Management, objet ResourceLocator
- Objet ResourceLocator Windows Remote Management, propriété ResourceURI
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28f804835b5445c32f74094e8280a598785d1526
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465955"
---
# <a name="resourcelocatorresourceuri-property"></a>ResourceLocator. ResourceURI, propriété

Obtient ou définit l' [*URI de ressource*](windows-remote-management-glossary.md) dans un objet [**ResourceLocator**](resourcelocator.md) . Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui identifie la ressource. Lors de la définition de l’URI de ressource pour un objet [**ResourceLocator**](resourcelocator.md) , l’URI doit contenir uniquement le chemin d’accès.

## <a name="remarks"></a>Notes

Voici un exemple de chemin d’accès approprié pour [**resourceuri**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri).

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

Le chemin d’accès suivant ne fonctionne pas, car il contient une clé pour une instance spécifique. Utilisez la méthode [**ResourceLocator. AddSelector**](resourcelocator-addselector.md) pour spécifier une instance particulière.

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**IWSManResourceLocator :: resourceuri** est la méthode C++ correspondante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





