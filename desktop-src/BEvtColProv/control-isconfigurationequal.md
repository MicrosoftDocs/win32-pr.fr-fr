---
description: Comparez l’argument à la configuration active du collecteur.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Méthode IsConfigurationEqual de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747788"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a>Méthode IsConfigurationEqual de la classe Control

Comparez l’argument à la configuration active du collecteur.

## <a name="syntax"></a>Syntaxe


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Configuration* \[ de dans\]
</dt> <dd>

Configuration à comparer à la configuration active.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

<dl> <dt>


</dt> <dd>

0

Échec

</dd> <dt>


</dt> <dd>

1

Succès

</dd> </dl>

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

 

 




