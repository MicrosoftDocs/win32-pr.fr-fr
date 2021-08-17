---
description: Effectue le suivi des demandes enfants générées à partir d’une demande parente.
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: Interface IWbemCausalityAccess (Wbemint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: a8c71d5b5f59a3b59fe3b639104bfa1fa2dcf9cd35764e37984759827ff7e92b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131391"
---
# <a name="iwbemcausalityaccess-interface"></a>Interface IWbemCausalityAccess

L’interface **IWbemCausalityAccess** effectue le suivi des demandes enfants générées à partir d’une demande parente. Vous pouvez obtenir un objet **IWbemCausalityAccess** à l’aide d’une interface de requête (QI) pour [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext). Chaque requête est identifiée par un identificateur global unique (GUID) et peut avoir une requête parente ou peut être une requête principale. Un GUID est un nombre 128 bits unique. Par exemple, 5b2fc63a-8AF4-44cb-960C-aefdced908d6.

## <a name="members"></a>Membres

L’interface **IWbemCausalityAccess** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWbemCausalityAccess** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWbemCausalityAccess** possède ces méthodes.



| Méthode                                                    | Description                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRequestId**](iwbemcausalityaccess-getrequestid.md) | Retourne un identificateur GUID unique pour une demande.<br/>                                                                                                              |
| [**IsChildOf**](iwbemcausalityaccess-ischildof.md)       | Détermine si une demande est un enfant d’une requête parente spécifiée. Une requête parent peut avoir plusieurs requêtes enfants, chacune identifiée par une valeur GUID unique.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemint. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API COM pour WMI](com-api-for-wmi.md)
</dt> </dl>

 

