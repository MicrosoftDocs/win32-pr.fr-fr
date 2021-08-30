---
title: SystemRestoreConfig, classe
description: Fournit des propriétés pour contrôler la fréquence de création de points de restauration planifiée et la quantité d’espace disque consommée sur chaque lecteur.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Restauration du système de la classe SystemRestoreConfig
- Restauration du système de la classe SystemRestoreConfig, Description
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a007249038bf342bc5516fd66caa32e3a84971dab71512d9d744b3cc9ba1872b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009449"
---
# <a name="systemrestoreconfig-class"></a>SystemRestoreConfig, classe

Fournit des propriétés pour contrôler la fréquence de création de points de restauration planifiée et la quantité d’espace disque consommée sur chaque lecteur.

## <a name="syntax"></a>Syntaxe

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a>Membres

La classe **SystemRestoreConfig** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SystemRestoreConfig** possède les propriétés suivantes.

<dl> <dt>

**DiskPercent**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Quantité maximale d’espace disque sur chaque lecteur qui peut être utilisée par la restauration du système. Cette valeur est spécifiée sous la forme d’un pourcentage de l’espace disque total. La valeur par défaut est 12 pour cent.

**Windows Vista :** Reçoit une valeur de la Service VSS (VSS). Il s’agit de la quantité maximale d’espace disque sur chaque lecteur qui peut être utilisée par la restauration du système. La valeur par défaut est 15% de l’espace disque total ou 30 pour cent de l’espace libre disponible, la valeur la plus petite étant retenue.

</dd> <dt>

**RPGlobalInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intervalle de temps absolu auquel les points de contrôle système planifiés sont créés, en secondes. La valeur par défaut est 86 400 (24 heures).

**Windows Vista :** Reçoit une valeur du planificateur de tâches pour la restauration du système. Zéro si la tâche est désactivée.

</dd> <dt>

**RPLifeInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intervalle de temps pendant lequel les points de restauration sont conservés, en secondes. Lorsqu’un point de restauration devient antérieur à cet intervalle spécifié, il est supprimé. La limite d’âge par défaut est de 90 jours.

**Windows Vista :** Reçoit la valeur **UINTMAX**.

</dd> <dt>

**RPSessionInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Intervalle de temps pendant lequel les points de contrôle du système planifiés sont créés au cours de la session, en secondes. La valeur par défaut est zéro, ce qui indique que la fonctionnalité est désactivée.

**Windows Vista :** Reçoit zéro si la restauration du système est désactivée.

</dd> </dl>

## <a name="examples"></a>Exemples

L’exemple de code suivant n’est pas pris en charge. Utilisez l’outil de ligne de commande Vssadmin.exe pour modifier la taille de l’espace réservé pour le lecteur.

**Windows XP :** Cet exemple est pris en charge.


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                         |
| Espace de noms<br/>                | Racine \\ par défaut<br/>                                                          |
| MOF<br/>                      | <dl> <dt>SR. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Points de restauration](restore-points.md)
</dt> <dt>

[Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

