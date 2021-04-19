---
title: Méthode IConfigAsfWriter ConfigureFilterUsingProfileId
description: La méthode ConfigureFilterUsingProfileId configure le filtre pour écrire un fichier ASF avec un index d’identificateur de profil (ID) à partir de la liste des profils système. (Pour les profils Windows Media format 4,0 uniquement.).
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Méthode ConfigureFilterUsingProfileId format Windows Media
- Méthode ConfigureFilterUsingProfileId format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode ConfigureFilterUsingProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510476"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a>IConfigAsfWriter :: ConfigureFilterUsingProfileId, méthode

La méthode **ConfigureFilterUsingProfileId** configure le filtre pour écrire un fichier ASF avec un index d’identificateur de profil (ID) à partir de la liste des profils système. (Pour les profils Windows Media format 4,0 uniquement.)

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwProfileId* \[ dans\]
</dt> <dd>

ID de profil tel que défini dans la version 4,0 du kit de développement logiciel (SDK) du format Windows Media.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                         | Description                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | S_OK<br/>        |
| <dl> <dt>**E \_ échec**</dt> </dl>              | Le profil n’est pas valide.<br/>    |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl> | Le graphique de filtre est arrêté.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode est désormais obsolète, car elle suppose les profils du kit de développement logiciel (SDK) de format Windows Media version 4,0. Pour configurer le filtre pour les profils version 7,0 et versions ultérieures, utilisez [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) ou [**IConfigAsfWriter :: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

