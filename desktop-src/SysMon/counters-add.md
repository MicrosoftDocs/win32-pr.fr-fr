---
title: Counters. Add, méthode
description: Ajoute une instance CounterItem à la collection.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Ajouter la méthode SysMon
- Ajouter la méthode SysMon, classe Counters
- Compteurs classe SysMon, méthode Add
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d8169980de00338c7fdd0b804013f986a5a7ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008862"
---
# <a name="countersadd-method"></a>Counters. Add, méthode

Ajoute une instance [**CounterItem**](counteritem.md) à la collection.

## <a name="syntax"></a>Syntaxe


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nom du chemin* \[ dans\]
</dt> <dd>

Chemin d’accès au compteur. Le chemin d’accès peut inclure un nom d’ordinateur et doit inclure un nom d’objet de performance, un nom d’instance d’objet si l’objet de performance spécifié prend en charge plusieurs instances et un nom de compteur. Cette spécification de chemin d’accès ne respecte pas la casse.

Pour plus d’informations sur la spécification d’un chemin d’accès de compteur, consultez [spécification d’un chemin d’accès de compteur](/windows/desktop/PerfCtrs/specifying-a-counter-path).

</dd> </dl>

## <a name="exceptions"></a>Exceptions




| Type d'exception | Condition | 
|----------------|-----------|
| <strong>System. Runtime. InteropServices. COMException</strong> | Vous pouvez recevoir cette exception pour l’une des raisons suivantes :<ul><li>L’objet de performance spécifié est introuvable sur l’ordinateur. La valeur de Err. Number est 0xC0000BB8.</li><li>Le compteur spécifié est introuvable. La valeur de Err. Number est 0xC0000BB9.</li></ul> | 




 

## <a name="remarks"></a>Notes

Si vous spécifiez un compteur de caractères génériques dans le paramètre *pathname* , la méthode **Add** crée un objet [**CounterItem**](counteritem.md) pour chaque chemin d’accès développé. La méthode **Add** retourne ensuite un pointeur vers le premier **CounterItem** ajouté.

Si le caractère générique se traduirait par un compteur dupliqué, l’erreur n’est pas signalée et aucun doublon n’est créé. Si une condition d’erreur se produit avant la création de tous les compteurs, l’erreur est signalée et les autres compteurs ne sont pas créés.

Il n’existe aucune limite au nombre de compteurs que vous pouvez ajouter. Toutefois, SYSMON affiche uniquement les premiers compteurs 1 024 de la collection. Il n’existe aucune limite quant au nombre de compteurs que SYSMON affiche dans un rapport.

Pour recevoir une notification lorsqu’un compteur est ajouté, implémentez l’événement [OnCounterAdded](systemmonitor-oncounteradded.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**SystemMonitor.BrowseCounters**](systemmonitor-browsecounters.md)
</dt> </dl>

 

