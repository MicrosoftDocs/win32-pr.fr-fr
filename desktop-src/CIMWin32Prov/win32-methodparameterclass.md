---
description: La \_ classe WMI MethodParameterClass abstraite de base dérive toute classe définie en tant que conteneur de valeurs de paramètre qui seront passées à une méthode.
ms.assetid: 293fa378-432d-4e97-a8ab-8dc4917d5476
ms.tgt_platform: multiple
title: Classe Win32_MethodParameterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MethodParameterClass
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e791941df681b2e46c4de6f0714b1290baecfde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123962"
---
# <a name="win32_methodparameterclass-class"></a>\_Classe MethodParameterClass Win32

La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MethodParameterClass** abstraite de base dérive toute classe définie en tant que conteneur de valeurs de paramètre qui seront passées à une méthode. Sans aucune propriété propre, cette classe sert de nœud de classification. Un exemple similaire est [**CIM \_ PhysicalElement**](cim-physicalelement.md). La dérivation à partir de **CIM \_ PhysicalElement** indique que la classe décrit une entité physique et non logique. Dans le cas de **\_ MethodParameterClass Win32**, les classes dérivées de celui-ci sont créées spécifiquement pour passer des paramètres à une méthode.

## <a name="syntax"></a>Syntaxe

## <a name="members"></a>Membres

La classe **Win32 \_ MethodParameterClass** ne définit aucun membre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes de gestion des services WMI](/windows/desktop/CIMWin32Prov/wmi-service-management-classes)
</dt> </dl>

 

