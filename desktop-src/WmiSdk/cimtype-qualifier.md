---
description: Le qualificateur CIMType contient le texte décrivant le type d’une propriété.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: Qualificateur CIMType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115867"
---
# <a name="cimtype-qualifier"></a>Qualificateur CIMType

Le qualificateur **CimType** contient le texte décrivant le type d’une propriété.

Ce texte peut être le type MOF, par exemple « String » et « sint32 » ou le type CIM, par exemple « CIM \_ String » et « CIM \_ sint32 ». Il existe une correspondance un-à-un entre le qualificateur **CimType** et le type de la propriété utilisée dans le paramètre *pvtType* de la méthode [**IWbemClassObject :: obtenir**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .

Les deux exceptions sont les suivantes :

-   [*Propriétés de référence*](gloss-r.md), qui ont le **type \_ référence CIM**, qui contient la valeur « Ref : ClassName ». La valeur ClassName décrit le type de classe de la propriété de référence.
-   Propriétés de l’objet incorporé, qui ont le type d' **\_ objet CIM** .

Notez, toutefois, que le qualificateur **CimType** peut et doit être utilisé pour taper une propriété de référence plus exactement. Par exemple, si la propriété fait toujours référence à des instances de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , son qualificateur **CimType** doit avoir la valeur :


```mof
"ref:Win32_LogicalDisk"
```



Par défaut, le qualificateur **CimType** d’une propriété de référence a le type **ref**.

Comme avec les propriétés de référence, le qualificateur **CimType** doit être utilisé pour taper une propriété d’objet incorporée plus exactement avec la syntaxe suivante :


```mof
"object:EmbedClass"
```



Étant donné que WMI autorise plus de types que ce qui peut être exprimé par des constantes standard avec le \_ préfixe VT, le qualificateur **CimType** peut aider à interpréter les valeurs de type. Le qualificateur **CimType** est ajouté automatiquement. Pour plus d’informations, consultez [types de données MOF](mof-data-types.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Qualificateurs WMI standard**](standard-wmi-qualifiers.md)
</dt> <dt>

[Qualificateurs WMI](wmi-qualifiers.md)
</dt> <dt>

[Ajout d’un qualificateur](adding-a-qualifier.md)
</dt> </dl>

 

