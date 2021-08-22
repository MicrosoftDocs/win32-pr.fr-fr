---
description: Définissez la nouvelle configuration active du collecteur.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Méthode SetConfiguration de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 41ff2c97eaa4b3e2080493c640b716ae4a822762b0f598c94e141a8cc4b4ac6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589069"
---
# <a name="setconfiguration-method-of-the-control-class"></a>Méthode SetConfiguration de la classe Control

Définissez la nouvelle configuration active du collecteur.

## <a name="syntax"></a>Syntaxe


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Configuration* \[ de dans\]
</dt> <dd>

Configuration à activer.

</dd> <dt>

*OldTimestampLow* \[ dans\]
</dt> <dd>

Bits de poids faible d’un horodatage qui indique quand la configuration active actuelle a été définie. La vérification de l’atomicité est activée si cette propriété n’a pas la valeur 0.

</dd> <dt>

*OldTimestampHigh* \[ dans\]
</dt> <dd>

Bits de poids fort d’un horodatage qui indique quand la configuration active actuelle a été définie. La vérification de l’atomicité est activée si cette propriété n’a pas la valeur 0.

</dd> <dt>

*NewTimestampLow* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée, ce paramètre contient les bits de poids faible d’un horodatage qui indique quand la nouvelle configuration a été définie. La vérification de l’atomicité est activée si cette propriété n’a pas la valeur 0.

</dd> <dt>

*NewTimestampHigh* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée, ce paramètre contient les bits de poids fort de l’horodatage qui indique quand la nouvelle configuration a été définie. La vérification de l’atomicité est activée si cette propriété n’a pas la valeur 0.

</dd> <dt>

*ErrorString* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée, en cas d’erreur, ce paramètre contient la description de l’erreur.

</dd> <dt>

*WarningString* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée, ce paramètre contient tous les messages d’avertissement relatifs à l’opération.

</dd> <dt>

*InfoString* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée, ce paramètre contient des informations relatives à la nouvelle configuration active.

</dd> <dt>

*ErrorType* \[ à\]
</dt> <dd>

Lorsque cette méthode est retournée, en cas d’erreur, ce paramètre indique le type d’erreur.

<dt>

0
</dt> <dd>

La nouvelle configuration est manquante.

</dd> <dt>

1
</dt> <dd>

Le format de la nouvelle configuration n’est pas valide.

</dd> <dt>

2
</dt> <dd>

La nouvelle configuration n’est pas valide.

</dd> <dt>

3
</dt> <dd>

Une erreur s’est produite en raison d’un socket ouvert.

</dd> <dt>

4
</dt> <dd>

Une erreur d’écriture de fichier s’est produite.

</dd> <dt>

5
</dt> <dd>

Une erreur d’atomicité s’est produite.

</dd> </dl> </dd> </dl>

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
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                       |
| Espace de noms<br/>                | racine \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Contrôler**](control.md)
</dt> </dl>

 

 




