---
description: IDelaydC ::P méthode ause-la méthode pause interrompt la capture en cours.
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: IDelaydC ::P méthode ause (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 21b4cd7b6cb921f7bd71b8670a37da12b2239b92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021089"
---
# <a name="idelaydcpause-method"></a>IDelaydC ::P méthode ause

La méthode **Pause** interrompt la capture en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                           | Description                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ suspendue**</dt> </dl> | La capture est déjà dans un état suspendu.<br/>                                                                                  |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>  | Le NPP ne capture pas de données. Appelez [IDelaydC :: Start](idelaydc-start.md) pour démarrer la capture.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>  | Le NPP n’est pas connecté au réseau. appelez [IDelaydC :: Connecter](idelaydc-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ retardé**</dt> </dl>    | le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connecter](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Notes

Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas ajoutées au [*fichier de capture*](c.md) actuel tant que la méthode **IDelaydC :: Resume** n’est pas appelée pour redémarrer la capture. Lorsque l' **interruption** et la **reprise** sont utilisées pour arrêter et redémarrer la capture, toutes les informations capturées sont placées dans le même fichier de capture.

Quand vous utilisez **IDelaydC ::P ause** et **IDelaydC :: Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) chaque fois que la capture est en cours d’exécution.

Pour redémarrer la capture, appelez [IDelaydC :: Resume](idelaydc-resume.md).

Pour arrêter la capture, appelez [IDelaydC :: Stop](idelaydc-stop.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC :: Connecter](idelaydc-connect.md)
</dt> <dt>

[IDelaydC :: Resume](idelaydc-resume.md)
</dt> <dt>

[IDelaydC :: Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC :: Stop](idelaydc-stop.md)
</dt> </dl>

 

 




