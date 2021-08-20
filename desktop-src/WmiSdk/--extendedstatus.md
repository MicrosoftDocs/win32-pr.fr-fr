---
description: Utilisé pour signaler des informations détaillées sur l’État et l’erreur.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: Classe __ExtendedStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0767215653895de6849e10174f0e66a63ade97e84bbf2b05410768e5e735d298
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926278"
---
# <a name="__extendedstatus-class"></a>\_\_ExtendedStatus, classe

La classe système **\_ \_ ExtendedStatus** est utilisée pour signaler des informations détaillées sur l’État et l’erreur.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ ExtendedStatus** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ ExtendedStatus** possède les propriétés suivantes.

<dl> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Toute chaîne définie par l’utilisateur qui décrit une erreur ou un état opérationnel.

</dd> <dt>

**opération**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Opération qui se produit au moment d’une défaillance ou d’une anomalie. en règle générale, Windows Management Instrumentation (WMI) définit cette propriété sur le nom d’une API COM pour la méthode WMI, telle que la suivante : [**IWbemServices :: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Paramètres impliqués dans une modification d’erreur ou d’État. Par exemple, si une application tente de récupérer une classe qui n’existe pas, cette propriété est définie sur le nom de la classe incriminée.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Identifie le fournisseur qui provoque ou signale une modification d’erreur ou d’État. si aucun fournisseur n’est impliqué, cette chaîne est définie sur « gestion de la Windows ».

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Contient une erreur ou un code d’information pour une opération. Il peut s’agir de n’importe quelle valeur définie par le fournisseur, mais la valeur 0 (zéro) est généralement réservée pour indiquer la réussite. Cette propriété est héritée de [**\_ \_ NotifyStatus**](--notifystatus.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ ExtendedStatus** est dérivée de la classe [**\_ \_ NotifyStatus**](--notifystatus.md) .

Utilisez la classe **\_ \_ ExtendedStatus** pour signaler des informations plus complexes qu’un code de résultat simple. Les fournisseurs peuvent dériver leurs propres classes à partir de **\_ \_ ExtendedStatus** s’ils requièrent plus de propriétés pour décrire les erreurs.

La propriété **statusCode** , héritée de la classe parente [**\_ \_ NotifyStatus**](--notifystatus.md) , est un entier non signé qui représente la valeur de l’erreur ou de l’État. Lorsque des instances de cette classe sont retournées par un fournisseur dynamique à partir d’une méthode, les propriétés **statusCode** et **Description** sont définies par le fournisseur, et les autres propriétés sont définies par WMI.

## <a name="examples"></a>Exemples

L’exemple de code suivant, extrait de l’exemple de code [FND : How to handle Configuration Manager des erreurs asynchrones à l’aide](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) de code WMI VBScript dans la Galerie TechNet, décrit l’utilisation de **\_ \_ ExtendedStatus** pour récupérer des informations d’erreur.


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

