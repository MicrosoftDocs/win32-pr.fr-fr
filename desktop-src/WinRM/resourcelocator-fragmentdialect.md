---
title: ResourceLocator. FragmentDialect, propriété (WSManDisp. h)
description: Obtient ou définit le dialecte de langage pour un dialecte de fragment de ressource quand ResourceLocator est utilisé dans les opérations d’objet de session telles que session. obtenir, session. put ou session. Enumerate.
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la propriété FragmentDialect
- Windows Remote Management de la propriété FragmentDialect, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, propriété FragmentDialect
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ae7cbbd71b4ccad24ecaa17d0fd635761f661bcd6dc95ebc0345e9164adcd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997299"
---
# <a name="resourcelocatorfragmentdialect-property"></a>ResourceLocator. FragmentDialect, propriété

Obtient ou définit le dialecte de langage pour un *dialecte* de [*fragment*](windows-remote-management-glossary.md) de [*ressource*](windows-remote-management-glossary.md) quand [**ResourceLocator**](resourcelocator.md) est utilisé dans les opérations d’objet de [**session**](session.md) telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md). Un fragment représente une propriété ou une partie d’une ressource. Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) . Le dialecte indique quel langage XML décrit le fragment au service qui implémente le [protocole WS-Management](ws-management-protocol.md) et reçoit la requête.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne XML qui identifie le langage utilisé dans la propriété [**FragmentPath**](resourcelocator-fragmentpath.md) . La chaîne de dialecte est par défaut la spécification XPath 1,0. Pour plus d’informations, consultez [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="remarks"></a>Remarques

[**IWSManResourceLocator :: FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) est la propriété C++ correspondante.

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

 

 





