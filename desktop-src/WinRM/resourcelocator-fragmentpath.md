---
title: ResourceLocator. FragmentPath, propriété (WSManDisp. h)
description: Obtient ou définit le chemin d’accès d’un fragment ou d’une propriété de ressource lorsque ResourceLocator est utilisé dans les opérations d’objet de session, telles que session. obtenir, session. put ou session. Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la propriété FragmentPath
- Windows Remote Management de la propriété FragmentPath, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, propriété FragmentPath
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032899"
---
# <a name="resourcelocatorfragmentpath-property"></a>ResourceLocator. FragmentPath, propriété

Obtient ou définit le chemin d’accès d’un [*fragment*](windows-remote-management-glossary.md) ou d’une propriété de [*ressource*](windows-remote-management-glossary.md) lorsque [**ResourceLocator**](resourcelocator.md) est utilisé dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui identifie le fragment ou la propriété de la ressource. Par exemple, si la ressource est un lecteur de disque et que la propriété demandée est fabricant, la chaîne peut contenir `Diskdrive/Manufacturer` . Le texte du fragment respecte la casse. Dans ce cas, vous ne pouvez pas utiliser `diskdrive/manufacturer` .

## <a name="remarks"></a>Notes

**IWSManResourceLocator :: FragmentPath** est la propriété C++ correspondante.

Vous pouvez spécifier un élément d’une propriété de tableau en fournissant l’index de tableau comme indiqué dans l’exemple suivant. N’oubliez pas que l’indexation de tableau commence par 1 au lieu de 0.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



Pour récupérer le tableau entier, spécifiez le nom de la propriété de tableau comme indiqué dans l’exemple suivant.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



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

 

 





