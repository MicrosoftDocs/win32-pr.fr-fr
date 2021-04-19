---
title: Méthode IConfigAsfWriter ConfigureFilterUsingProfile
description: La méthode ConfigureFilterUsingProfile est la méthode recommandée pour définir un profil. Il configure le filtre pour écrire un fichier ASF basé sur le profil défini par l’application spécifié.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Méthode ConfigureFilterUsingProfile format Windows Media
- Méthode ConfigureFilterUsingProfile format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode ConfigureFilterUsingProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513732"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a>IConfigAsfWriter :: ConfigureFilterUsingProfile, méthode

La méthode **ConfigureFilterUsingProfile** est la méthode recommandée pour définir un profil. Il configure le filtre pour écrire un fichier ASF basé sur le profil défini par l’application spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pProfile* \[ dans\]
</dt> <dd>

Pointeur vers l’interface [**IWMProfile**](iwmprofile.md) sur le profil défini par l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                                         | Description                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | S_OK<br/>                              |
| <dl> <dt>**\_pointeur E**</dt> </dl>           | Le pointeur d’interface **IWMProfile** n’est pas valide.<br/> |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl> | Le graphique est arrêté.<br/>                              |



 

## <a name="remarks"></a>Notes

En cas de réussite, cette méthode entraîne l’envoi d’un événement **\_ \_ Changed Graph** à l’application. Utilisez cette méthode pour configurer l’enregistreur avec un profil Windows Media 9 de la série personnalisé que vous avez créé (ou chargé à partir d’un fichier. prx existant) à l’aide des méthodes du kit de développement logiciel (SDK) du format Windows Media.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

