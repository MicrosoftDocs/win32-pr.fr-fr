---
title: Break, commande
description: La commande Break spécifie une clé pour abandonner une commande qui a été appelée à l’aide de \ 0034 ; Wait \ 0034 ; activé. Cette commande est une commande système MCI. elle est interprétée directement par MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- commande break Windows multimédia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363683"
---
# <a name="break-command"></a>Break, commande

La commande Break spécifie une clé pour abandonner une commande qui a été appelée à l’aide de l’indicateur « WAIT ». Cette commande est une commande système MCI. elle est interprétée directement par MCI.

Pour envoyer cette commande, appelez la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) avec le paramètre *lpszCommand* défini comme suit.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificateur d’un appareil MCI. Cet identificateur ou alias est attribué lorsque l’appareil est ouvert.

</dd> <dt>

<span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*
</dt> <dd>

Un des indicateurs suivants.



| Valeur                 | Signification                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| sur le *Code de touche virtuelle* | Spécifie la clé qui abandonne une commande qui a été démarrée à l’aide de l’indicateur « WAIT ». |
| arrêt                   | Désactive la clé d’arrêt actuelle.                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Peut être « Wait », « Notify », ou les deux. Pour les appareils vidéo numériques et VCR, vous pouvez également spécifier « test ». Pour plus d’informations sur ces indicateurs, consultez [les indicateurs d’attente, de notification et de test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Remarques

Lorsque la touche arrêt est activée et que l’utilisateur appuie sur la touche identifiée par le code de la touche virtuelle spécifiée dans le paramètre *lpszVirtKey* , l’appareil renvoie le contrôle à l’application. Si possible, la commande continue l’exécution.

## <a name="examples"></a>Exemples

La commande suivante définit F2 comme clé d’arrêt pour l’appareil « mySound ».

``` syntax
break mysound on 113
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Chaînes de commande MCI](mci-command-strings.md)
</dt> </dl>

 

