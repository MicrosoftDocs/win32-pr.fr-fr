---
description: Arrêtez rapidement le collecteur, en ignorant toutes les données mises en file d’attente.
ms.assetid: 9d96a94b-21ae-40bd-9c7f-b466ca38dce3
ms.tgt_platform: multiple
title: Méthode FastShutdown de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.FastShutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 444fe9c94e9fd247e5976fd67a43b0a5eee8b591
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515767"
---
# <a name="fastshutdown-method-of-the-control-class"></a>Méthode FastShutdown de la classe Control

Arrêtez rapidement le collecteur, en ignorant toutes les données mises en file d’attente.

## <a name="syntax"></a>Syntaxe


```mof
void FastShutdown();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                       |
| Espace de noms<br/>                | Racine \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Contrôler**](control.md)
</dt> </dl>

 

 




