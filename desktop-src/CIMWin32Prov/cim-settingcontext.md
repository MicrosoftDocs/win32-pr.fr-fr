---
description: La \_ classe SETTINGCONTEXT CIM associe les objets de configuration aux objets Setting.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: Classe CIM_SettingContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: df59bff8be90d3db3ac6dfde638120779850f2691bd3e93826c57f829d034a4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919509"
---
# <a name="cim_settingcontext-class"></a>\_Classe CIM SettingContext

La **classe \_ SettingContext CIM** associe les objets de configuration aux objets Setting. Par exemple, les paramètres d’une carte réseau peuvent changer en fonction du site ou du réseau auquel son système informatique d’hébergement est attaché. Dans ce cas, le système informatique a deux objets de configuration différents, qui correspondent aux différences de configuration réseau pour les deux segments de réseau. Une configuration agrège un objet de paramètre pour la carte réseau lors de l’utilisation d’un segment ; en revanche, l’autre configuration agrège un autre objet de paramètre de carte réseau, propre à un autre segment. Notez que de nombreux paramètres de l’ordinateur sont indépendants de la configuration du réseau. Par exemple, les deux configurations regroupent le même objet de paramètre pour la résolution de l’écran du système de l’ordinateur.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ SettingContext** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ SettingContext** possède les propriétés suivantes.

<dl> <dt>

**Contexte**
</dt> <dd> <dl> <dt>

Type de données **: \_ configuration CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Référence à l’objet de configuration qui agrège le paramètre.

</dd> <dt>

**Paramètre**
</dt> <dd> <dl> <dt>

Type de données **: \_ paramètre CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Référence à un paramètre agrégé.

</dd> </dl>

## <a name="remarks"></a>Remarques

WMI n’implémente pas cette classe.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

