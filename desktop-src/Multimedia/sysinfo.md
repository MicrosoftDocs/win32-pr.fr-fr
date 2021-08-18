---
title: commande sysinfo
description: La commande sysinfo récupère les informations système de MCI. La commande sysinfo est une commande système MCI. elle est interprétée directement par MCI.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- commande sysinfo Windows multimédia
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0af11370fd3968a2f5a6cf296ea04507f18d517665071674cfa8a4573e1a4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688329"
---
# <a name="sysinfo-command"></a>commande sysinfo

La commande sysinfo récupère les informations système de MCI. La commande sysinfo est une commande système MCI. elle est interprétée directement par MCI.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszDeviceID* 
</dt> <dd>

Identificateur d’un type d’appareil ou d’appareil MCI. Si un type d’appareil est spécifié, il doit s’agir d’un nom de type d’appareil MCI standard, tel qu’indiqué dans la documentation de référence de la commande [**Capability**](capability.md) . Vous pouvez spécifier « All » lorsque l’indicateur spécifié dans *lpszRequest* autorise cette possibilité.

</dd> <dt>

*lpszRequest* 
</dt> <dd>

Un des indicateurs suivants.



| Valeur                                                                                                                                                                | Signification                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <dt>**installname**</dt> </dl>               | Retourne le nom indiqué dans le registre ou le fichier SYSTEM.INI utilisé pour installer l’appareil ouvert avec l’identificateur de périphérique spécifié.<br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <dt>**spécifiée**</dt> </dl>                        | Retourne le nombre de périphériques MCI listés dans le registre ou le fichier SYSTEM.INI du type spécifié dans le paramètre *lpszDeviceID* . Cet identificateur de périphérique doit être un nom de type d’appareil MCI standard. Tous les chiffres après le type d’appareil sont ignorés. La spécification de « All » pour *lpszDeviceID* retourne le nombre total de périphériques MCI dans le système.<br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <dt>**quantité ouverte**</dt> </dl>         | Retourne le nombre d’appareils MCI ouverts du type spécifié dans *lpszDeviceID*. Cet identificateur de périphérique doit être un nom de type d’appareil MCI standard. Si vous spécifiez « All » pour *lpszDeviceID* , le nombre total d’appareils MCI ouverts dans le système est retourné.<br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <dt>* * nom * index * * *</dt> </dl>                | Retourne le nom d’un périphérique MCI. L’identificateur d’appareil doit être un nom de type d’appareil MCI standard. L' *index* est compris entre 1 et le nombre d’appareils de ce type. Si « ALL » est spécifié pour *lpszDeviceID*, *index* est compris entre 1 et le nombre total d’appareils dans le système.<br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <dt>***index* de nom ouvert**</dt> </dl> | Retourne le nom d’un périphérique MCI ouvert. L’identificateur d’appareil doit être un nom de type d’appareil MCI standard. L' *index* est compris entre 1 et le nombre d’appareils ouverts de ce type d’appareil. Si « ALL » est spécifié pour *lpszDeviceID*, *index* est compris entre 1 et le nombre total d’appareils ouverts dans le système.<br/>                                          |



 

</dd> <dt>

*lpszFlags* 
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="examples"></a>Exemples

La commande suivante retourne le nombre de périphériques audio Wave ouverts.

``` syntax
sysinfo waveaudio quantity open
```

La commande suivante renvoie le nom (l’alias d’appareil) du premier périphérique Wave-Audio ouvert.

``` syntax
sysinfo waveaudio name 1 open
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> <dt>

[**Faculté**](capability.md)
</dt> </dl>

 

