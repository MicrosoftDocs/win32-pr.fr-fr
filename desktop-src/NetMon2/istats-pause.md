---
description: La méthode pause arrête temporairement la capture en cours.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: IStats ::P méthode ause (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d1bab0d66a081c175d997e093d7dd1ff2b0d1c9622ecff73e0b3b1473edc885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495209"
---
# <a name="istatspause-method"></a>IStats ::P méthode ause

La méthode **Pause** arrête temporairement la capture en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                            | Description                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ suspendue**</dt> </dl>  | La capture est déjà suspendue.<br/>                                                                                                    |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>   | Le NPP ne capture pas de données. Appelez la méthode [IStats :: Start](istats-start.md) pour démarrer la capture.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>   | Le NPP n’est pas connecté au réseau. appelez la méthode [IStats :: Connecter](istats-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ stats \_ uniquement**</dt> </dl> | le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connecter](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Remarques

Lorsque la capture est suspendue, les nouveaux frames ne sont pas capturés tant qu’un appel à la méthode [IStats :: Resume](istats-resume.md) n’a pas redémarré la capture.

Lorsque vous utilisez les méthodes **IStats ::P ause** et **IStats :: Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) chaque fois que la capture est en cours d’exécution.

Pour redémarrer l’appel de capture [IStats :: Resume](istats-resume.md). Pour arrêter la capture, appelez [IStats :: Stop](istats-stop.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats :: Connecter](istats-connect.md)
</dt> <dt>

[IStats :: Resume](istats-resume.md)
</dt> <dt>

[IStats :: Start](istats-start.md)
</dt> <dt>

[IStats :: Stop](istats-stop.md)
</dt> </dl>

 

 




