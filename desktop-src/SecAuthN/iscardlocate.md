---
description: L’interface ISCardLocate fournit des services permettant de localiser une carte à puce par son nom.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Interface ISCardLocate (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193911"
---
# <a name="iscardlocate-interface"></a>Interface ISCardLocate

\[L’interface **ISCardLocate** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

L’interface **ISCardLocate** fournit des services permettant de localiser une [*carte à puce*](../secgloss/s-gly.md) par son nom.

Cette interface peut afficher l' [*interface utilisateur*](../secgloss/u-gly.md) de la carte à puce, si nécessaire.

Le scénario suivant illustre une utilisation type de l’interface **ISCardLocate** . L’interface **ISCardLocate** est utilisée pour générer une [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).

**Pour rechercher une carte spécifique à l’aide de son nom**

1.  Créer une interface **ISCardLocate** .
2.  Appelez [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) pour rechercher un nom de carte à puce.
3.  Appelez [**FindCard**](iscardlocate-findcard.md) pour rechercher la carte à puce.
4.  interpréter les résultats ;
5.  Libérez l’interface **ISCardLocate** .

## <a name="members"></a>Membres

L’interface **ISCardLocate** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardLocate** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISCardLocate** possède ces méthodes.



| Méthode                                                                  | Description                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| **ConfigureCardGuidSearch**                                             | Réservé pour un usage futur.<br/>                                        |
| [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) | Spécifie le nom de la carte à utiliser dans la recherche.<br/>               |
| [**FindCard**](iscardlocate-findcard.md)                               | Recherche la carte à puce et ouvre une connexion valide à celle-ci.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate est défini en tant que 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



 

 
