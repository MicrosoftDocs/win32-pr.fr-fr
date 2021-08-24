---
description: L’interface ISCardDatabase fournit les méthodes permettant d’effectuer les opérations de base de données du gestionnaire de ressources de carte à puce.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Interface ISCardDatabase (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a5bdad1db29630dcf029aab4fbc3812cfc83e0c69dab33c31edb73e21b297b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577169"
---
# <a name="iscarddatabase-interface"></a>Interface ISCardDatabase

\[L’interface **ISCardDatabase** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

L’interface **ISCardDatabase** fournit les méthodes permettant d’effectuer les opérations de base de données [*du gestionnaire de ressources*](../secgloss/r-gly.md) de [*carte à puce*](../secgloss/s-gly.md) . Ces opérations incluent la liste des cartes à puce, des [*lecteurs*](../secgloss/r-gly.md)et des groupes de lecteurs connus, ainsi que la récupération des interfaces prises en charge par une carte à puce et son [*fournisseur de services principal*](../secgloss/p-gly.md).

> [!Note]  
> L’identificateur du fournisseur de services principal est un GUID COM qui peut être utilisé pour instancier et utiliser les objets COM pour une carte spécifique.

 

L’exemple suivant illustre une utilisation type de l’interface **ISCardDatabase** . Dans ce cas, l’interface **ISCardDatabase** est utilisée pour répertorier toutes les cartes à puce connues.

**Pour soumettre une transaction à une carte spécifique**

1.  Créer une interface **ISCardDatabase** .
2.  Appelez [**ListCards**](iscarddatabase-listcards.md) pour récupérer toutes les cartes à puce connues en fonction d’une [*chaîne ATR*](../secgloss/a-gly.md) ou de leurs interfaces prises en charge.
3.  Libérez l’interface **ISCardDatabase** .

## <a name="members"></a>Membres

L’interface **ISCardDatabase** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardDatabase** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISCardDatabase** possède ces méthodes.



| Méthode                                                          | Description                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)   | Récupère l’identificateur du [*fournisseur de services principal*](../secgloss/p-gly.md) pour une carte à puce spécifique.<br/> |
| [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) | Récupère les identificateurs d’interface (GUID) de toutes les interfaces prises en charge par une carte à puce spécifique.<br/>                                                                                 |
| [**ListCards**](iscarddatabase-listcards.md)                   | Récupère tous les noms de carte à puce qui correspondent à un ensemble spécifique d’identificateurs d’interface (GUID) ou une [*chaîne ATR*](../secgloss/a-gly.md).<br/> |
| [**ListReaderGroups**](iscarddatabase-listreadergroups.md)     | Récupère les noms des groupes de [*lecteurs*](../secgloss/r-gly.md) que le gestionnaire de ressources a connaissance de.<br/>                        |
| [**ListReaders**](iscarddatabase-listreaders.md)               | Récupérez les noms des [*lecteurs*](../secgloss/r-gly.md) dont le gestionnaire de ressources a connaissance.<br/>                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardDatabase est défini en tant que 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



 

 
