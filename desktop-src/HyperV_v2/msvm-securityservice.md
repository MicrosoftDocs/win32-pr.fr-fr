---
description: Représente le service de sécurité. Il est utilisé pour configurer les paramètres de sécurité du système virtuel.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952125"
---
# <a name="msvm_securityservice-class"></a>MSVM \_ securityservice, classe

Représente le service de sécurité. Il est utilisé pour configurer les paramètres de sécurité du système virtuel.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ securityservice** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ securityservice** possède ces méthodes.



| Méthode                                                                                            | Description                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**GetKeyProtector**](msvm-securityservice-getkeyprotector.md)                                   | Méthode permettant de récupérer le protecteur de clé pour un système virtuel.<br/>   |
| [**ModifySecuritySettings**](msvm-securityservice-modifysecuritysettings.md)                     | Modifie les paramètres de sécurité actuels d’un ordinateur virtuel.<br/> |
| [**RestoreLastKnownGoodKeyProtector**](msvm-securityservice-restorelastknowngoodkeyprotector.md) | Méthode pour restaurer le dernier protecteur de clé valide connu.<br/> |
| [**SetKeyProtector**](msvm-securityservice-setkeyprotector.md)                                   | Méthode permettant de définir le protecteur de clé pour un système virtuel.<br/>        |
| [**SetSecurityPolicy**](msvm-securityservice-setsecuritypolicy.md)                               | Méthode permettant de définir le protecteur de clé pour un système virtuel.<br/>        |
| [**StartService**](msvm-securityservice-startservice.md)                                         | démarre le service.<br/>                                          |
| [**StopService**](msvm-securityservice-stopservice.md)                                           | arrête le service.<br/>                                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service CIM**](cim-service.md)
</dt> </dl>

 

 




