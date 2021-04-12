---
title: Méthode IMsTscAxEvents OnRemoteDesktopSizeChange
description: Appelé pour indiquer que la taille du contrôle client sur le Bureau à distance a changé en réponse à une opération de contrôle client.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRemoteDesktopSizeChange
- Méthode OnRemoteDesktopSizeChange Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRemoteDesktopSizeChange
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508758"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a>IMsTscAxEvents :: OnRemoteDesktopSizeChange, méthode

Appelé pour indiquer que la taille du contrôle client sur le Bureau à distance a changé en réponse à une opération de contrôle client.

## <a name="syntax"></a>Syntaxe


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*largeur* \[ dans\]
</dt> <dd>

Largeur, en pixels, du Bureau à distance redimensionné.

</dd> <dt>

*hauteur* \[ dans\]
</dt> <dd>

Hauteur, en pixels, du Bureau à distance redimensionné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cet événement permet au conteneur de déterminer s’il doit se redimensionner en réponse à une opération de contrôle client, ce qui peut entraîner une plus grande taille de bureau affichable. Notez que le contrôle ajuste automatiquement les barres de défilement pour la nouvelle taille de session.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





