---
description: La méthode pause interrompt la capture en cours.
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
ms.openlocfilehash: d44ae7792388d9ca637232b45e63d618a37acb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861994"
---
# <a name="idelaydcpause-method"></a>IDelaydC ::P méthode ause

La méthode **Pause** interrompt la capture en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                           | Description                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ suspendue**</dt> </dl> | La capture est déjà dans un état suspendu.<br/>                                                                                  |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>  | Le NPP ne capture pas de données. Appelez [IDelaydC :: Start](idelaydc-start.md) pour démarrer la capture.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>  | Le NPP n’est pas connecté au réseau. Appelez [IDelaydC :: Connect](idelaydc-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ retardé**</dt> </dl>    | Le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connect](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Notes

Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas ajoutées au [*fichier de capture*](c.md) actuel tant que la méthode **IDelaydC :: Resume** n’est pas appelée pour redémarrer la capture. Lorsque l' **interruption** et la **reprise** sont utilisées pour arrêter et redémarrer la capture, toutes les informations capturées sont placées dans le même fichier de capture.

Quand vous utilisez **IDelaydC ::P ause** et **IDelaydC :: Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) chaque fois que la capture est en cours d’exécution.

Pour redémarrer la capture, appelez [IDelaydC :: Resume](idelaydc-resume.md).

Pour arrêter la capture, appelez [IDelaydC :: Stop](idelaydc-stop.md).

## <a name="requirements"></a>Configuration requise



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

[IDelaydC :: Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC :: Resume](idelaydc-resume.md)
</dt> <dt>

[IDelaydC :: Start](idelaydc-start.md)
</dt> <dt>

[IDelaydC :: Stop](idelaydc-stop.md)
</dt> </dl>

 

 




