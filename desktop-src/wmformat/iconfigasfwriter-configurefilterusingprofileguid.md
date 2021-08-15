---
title: Méthode IConfigAsfWriter ConfigureFilterUsingProfileGuid
description: La méthode ConfigureFilterUsingProfileGuid configure le filtre pour écrire un fichier ASF basé sur le profil prédéfini spécifié. (Déconseillé.).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Méthode ConfigureFilterUsingProfileGuid format Windows Media
- Méthode ConfigureFilterUsingProfileGuid format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode ConfigureFilterUsingProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f427dc67695ebaca3e3e7502f2f1961b738a8f775ace394948ef445f3ad9a64e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703085"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>IConfigAsfWriter :: ConfigureFilterUsingProfileGuid, méthode

La méthode **ConfigureFilterUsingProfileGuid** configure le filtre pour écrire un fichier ASF basé sur le profil prédéfini spécifié. (Déconseillée).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*guidProfile* \[ dans\]
</dt> <dd>

**GUID** identifiant un profil tel que défini dans le fichier d’en-tête du kit de développement logiciel (SDK) Windows Media Format Wmsysprf. h.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                         | Description                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | S_OK<br/>        |
| <dl> <dt>**E \_ échec**</dt> </dl>              | Le profil n’est pas valide.<br/>    |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl> | Le graphique de filtre est arrêté.<br/> |



 

## <a name="remarks"></a>Remarques

à partir du kit de développement logiciel (SDK) Windows Media Format 9 Series, aucun nouveau profil système n’a été défini. Seuls les GUID de profil système de version 8 (ou version antérieure) peuvent être utilisés avec cette méthode.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

