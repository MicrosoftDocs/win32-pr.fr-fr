---
description: 'Msvm_FcDeviceSAPImplementation Class : représente une association entre un point d’accès au service et l’appareil logique qui l’implémente.'
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Classe Msvm_FcDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b0df7a198b3ee52d131800073f8be30d51d93181
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119027"
---
# <a name="msvm_fcdevicesapimplementation-class"></a>MSVM \_ FcDeviceSAPImplementation, classe

Représente une association entre un point d’accès de service et l’appareil logique qui l’implémente. La cardinalité de cette association est plusieurs-à-plusieurs. Un point d’accès au service (SAP) peut être fourni par plusieurs unités logiques, fonctionnant conjointement. N’importe quel appareil peut fournir plusieurs SAP. Lorsque de nombreux périphériques logiques sont associés à un seul SAP, il est supposé que ces éléments fonctionnent conjointement pour fournir le point d’accès. Si différentes implémentations d’un SAP existent, chacune de ces implémentations entraînerait des instanciations individuelles de l’objet SAP. Ces instanciations individuelles ont ensuite des associations avec les implémentations uniques.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ FcDeviceSAPImplementation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ FcDeviceSAPImplementation** possède les propriétés suivantes.

<dl> <dt>

**Antécédent**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ FCPort**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Référence à une classe dérivée de **CIM \_ FCPort** qui représente l’appareil logique.

</dd> <dt>

**Charge**
</dt> <dd> <dl> <dt>

Type de données : **MSVM \_ FcEndpoint**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »)
</dt> </dl>

Référence à une instance de la classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) qui représente le SAP qui utilise l' **antécédent**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

