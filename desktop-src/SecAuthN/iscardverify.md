---
description: Fournit des services pour définir le code des IVT (vérification du détenteur de la carte) et pour vérifier l’utilisateur.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Interface ISCardVerify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757017"
---
# <a name="iscardverify-interface"></a>Interface ISCardVerify

\[L’interface **ISCardVerify** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La définition d’interface suivante est fournie en tant que norme qui peut être suivie lors du développement d’un [*fournisseur de services*](../secgloss/c-gly.md)de [*carte à puce*](../secgloss/s-gly.md) . L’interface **ISCardVerify** fournit des services pour définir le code des IVT (vérification du détenteur de la carte) et pour vérifier l’utilisateur.

La classe **ISCardVerify** est définie pour les applications qui implémentent la stratégie IVT propre à l’application et qui ont une connaissance détaillée de l’implémentation interne de la carte à puce.

Voici une utilisation courante de l’interface **ISCardVerify** .

La procédure suivante utilise **ISCardVerify** pour modifier le code des IVT.

**Pour modifier le code IVT d’une carte à puce**

1.  Créez une interface **ISCardVerify** (à l’aide de la méthode d’interface [**ISCardManage**](iscardmanage.md) correspondante).
2.  Appelez la méthode [**ChangeCode**](iscardverify-changecode.md) et fournissez un nouveau code, en spécifiant s’il est local ou global et s’il est activé ou désactivé.
3.  Libérez l’interface **ISCardVerify** .

## <a name="members"></a>Membres

L’interface **ISCardVerify** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardVerify** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISCardVerify** possède ces méthodes.



| Méthode                                                        | Description                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeCode**](iscardverify-changecode.md)                 | Modifie le code IVT actuel.<br/>                                                                                                    |
| [**ResetSecurityState**](iscardverify-resetsecuritystate.md) | Réinitialise le [*contexte de sécurité*](../secgloss/s-gly.md) de la carte à puce.<br/> |
| [**Verrouillage**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))                       | Réactive le contexte de [*sécurité*](../secgloss/s-gly.md).<br/>               |
| [**Vérifier**](iscardverify-verify.md)                         | Authentifie l’utilisateur.<br/>                                                                                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



 

 
