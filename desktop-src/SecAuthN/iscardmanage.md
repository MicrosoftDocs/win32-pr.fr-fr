---
description: Utilisé pour l’attachement à une carte à puce ou un lecteur spécifique, afin de créer d’autres interfaces facultatives pour exécuter des fonctions de carte à puce spécifiques, pour verrouiller une carte à puce spécifique pour une utilisation exclusive et pour obtenir l’état d’une carte à puce ou d’un lecteur.
ms.assetid: 67077034-5bd0-4176-9dc7-774caba3d427
title: Interface ISCardManage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage
api_type:
- COM
api_location: ''
ms.openlocfilehash: c027ae9004a8437f3d182fdef3335c8fbbad67abaab5c15e351520f2ae592818
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922648"
---
# <a name="iscardmanage-interface"></a>Interface ISCardManage

\[l’interface **ISCardManage** ne peut plus être utilisée à partir de Windows server 2008, Windows Vista et Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La définition d’interface suivante est fournie en tant que norme qui peut être suivie lors du développement d’un [*fournisseur de services*](../secgloss/c-gly.md)de [*carte à puce*](../secgloss/s-gly.md) .

L’interface **ISCardManage** doit être fournie. Il est utilisé pour l’attachement à une [*carte à puce*](../secgloss/s-gly.md) ou à un [*lecteur*](../secgloss/r-gly.md)spécifique, afin de créer d’autres interfaces facultatives pour exécuter des fonctions de carte à puce spécifiques, pour verrouiller une carte à puce spécifique en vue d’une utilisation exclusive et pour obtenir l’état d’une carte à puce ou d’un lecteur. En tant qu’ensemble, ces services peuvent être responsables de la maintenance d’un contexte bien défini dans lequel une application peut communiquer avec une [*carte à puce*](../secgloss/s-gly.md) ou un [*lecteur*](../secgloss/r-gly.md).

Voici une utilisation courante de l’interface **ISCardManage** .

**Pour se connecter à une carte à puce**

1.  Créez l’interface **ISCardManage** associée à la carte.
2.  Connecter à une carte à puce en l’attachant à un lecteur de carte à puce spécifique ([**AttachByIFD**](iscardmanage-attachbyifd.md)) ou à l’aide d’un handle précédemment acquis ([**AttachByHandle**](iscardmanage-attachbyhandle.md)).
3.  Créez d’autres interfaces pour effectuer des opérations de carte à puce ([**CreateCardAuth**](iscardmanage-createcardauth.md), [**CreateFileAccess**](iscardmanage-createfileaccess.md), [**CreateCHVerification**](iscardmanage-createchverification.md)ou [**CreateInterface**](iscardmanage-createinterface.md)).
4.  Relâchez la carte ([**détacher**](iscardmanage-detach.md)).
5.  Libérez l’interface **ISCardManage** et d’autres en fonction des besoins.

## <a name="members"></a>Membres

L’interface **ISCardManage** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardManage** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISCardManage** possède ces méthodes.



| Méthode                                                            | Description                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscardmanage-attachbyhandle.md)             | Permet à une application de créer un lien de communication vers une carte à puce à l’aide d’un handle renvoyé par le [*Gestionnaire de ressources*](../secgloss/r-gly.md)de carte à puce.<br/>                                              |
| [**AttachByIFD**](iscardmanage-attachbyifd.md)                   | Permet à une application de demander l’établissement d’un contexte pour un lecteur spécifique référencé avec un nom d’affichage.<br/>                                                                                                                                               |
| [**CreateCardAuth**](iscardmanage-createcardauth.md)             | Autorise la création d’une interface [**ISCardAuth**](iscardauth.md) .<br/>                                                                                                                                                                                            |
| [**CreateCHVerification**](iscardmanage-createchverification.md) | Autorise la création d’une interface [**ISCardVerify**](iscardverify.md) .<br/>                                                                                                                                                                                        |
| [**CreateFileAccess**](iscardmanage-createfileaccess.md)         | Autorise la création d’une interface [**ISCardFileAccess**](iscardfileaccess.md) .<br/>                                                                                                                                                                                |
| [**CreateInterface**](iscardmanage-createinterface.md)           | Autorise la création d’une interface.<br/>                                                                                                                                                                                                                            |
| [**Detach**](iscardmanage-detach.md)                             | Libère la pièce jointe d’une carte à puce ou d’un lecteur spécifique, respectivement allouée par [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md) .<br/>                                                                |
| [**Reconnexion**](iscardmanage-reconnect.md)                       | Permet à une application de se reconnecter à une carte à puce ou à un lecteur sans avoir à émettre un [**détachement**](iscardmanage-detach.md) suivi de [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md) , respectivement.<br/> |
| [**SCardLock**](iscardmanage-scardlock.md)                       | Verrouille une carte à puce ou un lecteur connecté pour une utilisation exclusive.<br/>                                                                                                                                                                                                       |
| [**SCardUnlock**](iscardmanage-scardunlock.md)                   | Libère l’utilisation exclusive de la carte à puce ou du lecteur connecté.<br/>                                                                                                                                                                                                   |
| [**Statut**](iscardmanage-status.md)                             | Permet à une application d’afficher l’état actuel de la carte à puce ou du lecteur.<br/>                                                                                                                                                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



 

 
