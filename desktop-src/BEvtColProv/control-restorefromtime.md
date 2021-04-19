---
description: Restaure la configuration active du collecteur à partir d’un fichier de sauvegarde, sélectionné par un horodateur.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Méthode RestoreFromTime de la classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516399"
---
# <a name="restorefromtime-method-of-the-control-class"></a>Méthode RestoreFromTime de la classe Control

Restaure la configuration active du collecteur à partir d’un fichier de sauvegarde, sélectionné par un horodateur.

## <a name="syntax"></a>Syntaxe


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TargetTimestampLow* \[ dans\]
</dt> <dd>

Restaurez le fichier de sauvegarde à cet horodateur. Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*TargetTimestampHigh* \[ dans\]
</dt> <dd>

Restaurez le fichier de sauvegarde à cet horodateur. Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampLow* \[ dans\]
</dt> <dd>

Horodateur de la définition de la configuration précédente. Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between). Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ dans\]
</dt> <dd>

Horodateur de la définition de la configuration précédente. Si la valeur est égale à 0, active la vérification de l’atomicité : la nouvelle configuration est appliquée uniquement si l’horodateur de l’ancienne configuration correspond (c.-à-d. que la configuration n’a pas été modifiée dans between). Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampLow* \[ à\]
</dt> <dd>

Horodateur de la définition de la nouvelle configuration, si l’appel a échoué. Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampHigh* \[ à\]
</dt> <dd>

Horodateur de la définition de la nouvelle configuration, si l’appel a échoué. Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampLow* \[ à\]
</dt> <dd>

Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois. Il s’agit de la partie basse de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ à\]
</dt> <dd>

Horodateur d’origine de lorsque la configuration restaurée a été définie pour la première fois. Il s’agit de la partie haute de [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

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

Type de l’erreur : Notez que 0 ou absent indique une réussite.

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
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Contrôler**](control.md)
</dt> </dl>

 

