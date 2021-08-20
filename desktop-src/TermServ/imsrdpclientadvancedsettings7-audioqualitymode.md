---
title: IMsRdpClientAdvancedSettings7 propriété AudioQualityMode
description: Spécifie ou récupère une valeur qui indique le paramètre de mode de qualité audio pour le son Redirigé. Par défaut, cette valeur est définie sur 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AudioQualityMode
- Services Bureau à distance de la propriété AudioQualityMode, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété AudioQualityMode
- Services Bureau à distance de la propriété AudioQualityMode, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété AudioQualityMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1635c2ed01144a640b624a014959a4847ae5f746502267444d958a20b959eef9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001307"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a>IMsRdpClientAdvancedSettings7 :: AudioQualityMode, propriété

Spécifie ou récupère une valeur qui indique le paramètre de mode de qualité audio pour le son Redirigé. Par défaut, cette valeur est définie sur 0.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a>Valeur de la propriété

Valeur qui spécifie le mode de qualité audio.

Les valeurs possibles sont les suivantes :

<dt>

0
</dt> <dd>

Qualité audio dynamique. Il s’agit du paramètre de qualité audio par défaut. Le serveur ajuste de manière dynamique la qualité de sortie audio en réponse aux conditions du réseau et aux fonctionnalités du client et du serveur.

</dd> <dt>

1
</dt> <dd>

Qualité audio moyenne. Le serveur utilise un format fixe mais compressé pour la sortie audio.

</dd> <dt>

2
</dt> <dd>

Haute qualité audio. Le serveur fournit une sortie audio au format PCM non compressé avec une charge de traitement inférieure pour la latence.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                                |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





