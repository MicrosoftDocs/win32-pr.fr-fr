---
description: L' \_ objet de configuration CIM permet de regrouper des jeux de paramètres (définis dans les \_ objets de paramètre CIM) et des dépendances pour un ou plusieurs éléments système gérés.
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: Classe CIM_Configuration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c6df2338d46438bf3e1af371ebbce8b36f1a337f26a4785064119cca45bece46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924929"
---
# <a name="cim_configuration-class"></a>\_Classe de configuration CIM

L’objet de **\_ configuration CIM** permet de regrouper des jeux de paramètres (définis dans les objets de [**\_ paramètre CIM**](cim-setting.md) ) et des dépendances pour un ou plusieurs éléments système gérés. Cet objet représente un certain comportement ou un état fonctionnel souhaité pour les éléments système gérés. L’état fonctionnel souhaité est généralement piloté par des exigences externes, telles que l’heure ou l’emplacement. Par exemple, pour se connecter à un système de messagerie à partir de chez vous, il existe une dépendance sur un modem. en revanche, il existe une dépendance sur une carte réseau au travail. Paramètres pour les appareils logiques pertinents (dans cet exemple, modem POTS et carte réseau) peuvent être définis et regroupés par **\_ Configuration CIM**. par conséquent, deux configurations « Connecter à la messagerie » peuvent être définies en regroupant les dépendances pertinentes et les objets de [**\_ paramètre CIM**](cim-setting.md) .

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a>Membres

La classe de **\_ configuration CIM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ configuration CIM** possède ces propriétés.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Description textuelle courte de l’objet de **\_ configuration CIM** .

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description textuelle de l’objet de **\_ configuration CIM** .

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Étiquette par laquelle l’objet de **\_ configuration CIM** est connu.

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



 

