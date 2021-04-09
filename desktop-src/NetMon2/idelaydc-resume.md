---
description: La méthode Resume redémarre une capture suspendue.
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'IDelaydC :: Resume, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750060"
---
# <a name="idelaydcresume-method"></a>IDelaydC :: Resume, méthode

La méthode **Resume** redémarre une capture suspendue.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                                | Description                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ non \_ suspendue**</dt> </dl> | La capture n’est pas suspendue. Appelez [**IDelaydC ::P ause**](idelaydc-pause.md) pour suspendre la capture.<br/>                                |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>       | Le NPP n’est pas connecté au réseau. Appelez [**IDelaydC :: Connect**](idelaydc-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ retardé**</dt> </dl>         | Le NPP est connecté au réseau, mais pas avec la méthode [**IDelaydC :: Connect**](idelaydc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Notes

Lorsque la capture est suspendue, les nouvelles données ne sont pas ajoutées au [*fichier de capture*](c.md) actuel tant que la méthode **IDelaydC :: Resume** n’est pas appelée pour redémarrer la capture. Lorsque l' [**interruption**](idelaydc-pause.md) et la **reprise** sont utilisées pour arrêter et redémarrer la capture, toutes les informations capturées sont placées dans le même fichier de capture.

Lorsque vous utilisez [**suspendre**](idelaydc-pause.md) et **reprendre** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) aux statistiques existantes pour la capture actuelle.

Pour arrêter la capture, appelez [**IDelaydC :: Stop**](idelaydc-stop.md).

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

[**IDelaydC :: Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC ::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC :: Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




