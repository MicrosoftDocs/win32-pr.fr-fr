---
description: 'Classe Msvm_WiFiDeviceSAPImplementation : association entre un point d’accès de service (SAP) et la façon dont il est implémenté.'
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Classe Msvm_WiFiDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99826ce3a37e19867cef1a6ddf276f5136b21a3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109247"
---
# <a name="msvm_wifidevicesapimplementation-class"></a>MSVM \_ WiFiDeviceSAPImplementation, classe

Association entre un point d’accès de service (SAP) et son implémentation. La cardinalité de cette association est plusieurs-à-plusieurs. Un SAP peut être fourni par plusieurs unités logiques, fonctionnant conjointement. N’importe quel appareil peut fournir plusieurs SAP. Lorsque de nombreux périphériques logiques sont associés à un seul SAP, il est supposé que ces éléments fonctionnent conjointement pour fournir le point d’accès. Si différentes implémentations d’un SAP existent, chacune de ces implémentations entraînerait des instanciations individuelles de l’objet SAP. Ces instanciations individuelles ont ensuite des associations avec les implémentations uniques.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ WiFiDeviceSAPImplementation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ WiFiDeviceSAPImplementation** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ WiFiPort**](msvm-wifiport.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Instance de la classe [**MSVM \_ WiFiPort**](msvm-wifiport.md) qui représente l’appareil logique.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ WiFiEndpoint**](msvm-wifiendpoint.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Instance de la classe [**MSVM \_ WiFiEndpoint**](msvm-wifiendpoint.md) qui représente le point d’accès au service implémenté à l’aide de l’unité logique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

