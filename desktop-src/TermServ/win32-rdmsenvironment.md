---
title: Classe Win32_RDMSEnvironment
description: Gère un environnement Bureau à distance Management Services (RDMS).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSEnvironment de la classe Services Bureau à distance
- Win32_RDMSEnvironment de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509712"
---
# <a name="win32_rdmsenvironment-class"></a>\_Classe RDMSEnvironment Win32

Gère un environnement Bureau à distance Management Services (RDMS).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDMSEnvironment** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ RDMSEnvironment** possède ces méthodes.



| Méthode                                                                   | Description                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetActiveServer**](getactiveserver-win32-rdmsenvironment.md)         | Récupère le nom de domaine complet (FQDN) de l’environnement RDMS.<br/>                 |
| [**GetClientAccessName**](getclientaccessname-win32-rdmsenvironment.md) | Récupère le nom de l’enregistrement de ressource (RR) DNS (Domain Name System) de l’environnement RDMS.<br/> |
| [**SetActiveServer**](setactiveserver-win32-rdmsenvironment.md)         | Définit le nom de domaine complet de l’environnement RDMS sur le nœud actuel.<br/>                                |
| [**SetClientAccessName**](setclientaccessname-win32-rdmsenvironment.md) | Met à jour le nom de l’enregistrement de ressource DNS de l’environnement RDMS.<br/>                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fournisseur de services de gestion Bureau à distance](rdms-api-reference.md)
</dt> </dl>

 

 





