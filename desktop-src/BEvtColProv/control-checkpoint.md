---
description: Si la configuration actuelle est un résultat de l’opération d’annulation/de rétablissement/restauration, le marque comme s’il avait été défini explicitement, afin que l’historique conserve l’heure à laquelle il a été défini, et un fichier de sauvegarde sera créé pour celui-ci lors de la prochaine modification de configuration.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Méthode Checkpoint de la classe Control (Srrestoreptapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 44453f647d55f29a9a6cfc5622e29dcc88ad2446
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110063"
---
# <a name="checkpoint-method-of-the-control-class"></a>Méthode Checkpoint de la classe Control

Si la configuration actuelle est un résultat de l’opération d’annulation/de rétablissement/restauration, le marque comme s’il avait été défini explicitement, afin que l’historique conserve l’heure à laquelle il a été défini, et un fichier de sauvegarde sera créé pour celui-ci lors de la prochaine modification de configuration. Si la configuration actuelle a déjà été définie explicitement, n’a aucun effet.

## <a name="syntax"></a>Syntaxe


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OldTimestampLow* \[ dans\]
</dt> <dd>

Horodatage de la définition de la configuration actuelle. Si la valeur est égale à 0, active la vérification de l’atomicité : l’action sera appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c’est-à-dire que la configuration n’a pas été modifiée dans between). Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ dans\]
</dt> <dd>

Horodatage de la définition de la configuration actuelle. Si la valeur est égale à 0, active la vérification de l’atomicité : l’action sera appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c’est-à-dire que la configuration n’a pas été modifiée dans between). Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*ErrorString* \[ à\]
</dt> <dd>

Chaîne de texte avec une explication de l’erreur.

</dd> <dt>

*WarningString* \[ à\]
</dt> <dd>

Chaîne de texte avec des avertissements.

</dd> <dt>

*InfoString* \[ à\]
</dt> <dd>

Chaîne de texte contenant des informations sur la configuration.

</dd> <dt>

*ErrorType* \[ à\]
</dt> <dd>

Type de l'erreur. Notez que 0 ou absent indique une réussite.

<dt>

0
</dt> <dd>

Réussite.

</dd> <dt>

1
</dt> <dd>

format d’argument incorrect

</dd> <dt>

2
</dt> <dd>

valeur d’argument incorrecte

</dd> <dt>

3
</dt> <dd>

erreur d’ouverture de ressource (Socket)

</dd> <dt>

4
</dt> <dd>

erreur de persistance (écriture de fichier)

</dd> <dt>

5
</dt> <dd>

erreur d’atomicité (l’ancien horodatage ne correspond pas)

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                       |
| Espace de noms<br/>                | Racine \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| En-tête<br/>                   | <dl> <dt>Srrestoreptapi. h</dt> </dl>          |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Contrôler**](control.md)
</dt> </dl>

 

