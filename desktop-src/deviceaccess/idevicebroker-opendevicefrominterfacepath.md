---
title: Méthode IDeviceBroker OpenDeviceFromInterfacePath
description: Tente d’ouvrir une instance d’interface d’appareil pour le compte d’un client. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- Méthode OpenDeviceFromInterfacePath API Broker d’accès du périphérique
- Méthode OpenDeviceFromInterfacePath API Broker d’accès du périphérique, interface IDeviceBroker
- API Broker d’accès du périphérique de l’interface IDeviceBroker, méthode OpenDeviceFromInterfacePath
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521785"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a>IDeviceBroker :: OpenDeviceFromInterfacePath, méthode

> [!Important]  
> Ces interfaces ne sont pas prises en charge et ne doivent pas être utilisées. Utilisez plutôt les API dans la [référence de programmation C++ de l’API d’accès à l’appareil](device-access-api-c---programming-reference.md) .

Tente d’ouvrir une instance d’interface d’appareil pour le compte d’un client. IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszDeviceInterfacePath* \[ dans\]
</dt> <dd>

Instance d’interface d’appareil à ouvrir.

</dd> <dt>

*desiredAccess* \[ dans\]
</dt> <dd>

Accès souhaité à passer à Open.

</dd> <dt>

*shareMode* \[ dans\]
</dt> <dd>

Mode de partage à passer à l’ouverture.

</dd> <dt>

*flagsAndAttributes* \[ dans\]
</dt> <dd>

Indicateurs et attributs à passer à Open.

</dd> <dt>

*\* phDevice* \[\]
</dt> <dd>

Handle résultant si la tentative d’ouverture a réussi.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette fonction est réussie, elle retourne S_OK. Sinon, elle retourne un code d’erreur HRESULT.
