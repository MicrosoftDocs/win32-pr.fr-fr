---
description: 'IDelaydC :: Start, méthode-la méthode start démarre une capture.'
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'IDelaydC :: Start, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 750a33241358aee924ed3f91491185117a77a548a87bdfc5514d59fe4798a42c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365864"
---
# <a name="idelaydcstart-method"></a>IDelaydC :: Start, méthode

La méthode **Start** démarre une capture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFileName* \[ à\]
</dt> <dd>

Pointeur vers le nom du [*fichier de capture*](c.md) utilisé pour stocker les données réseau. Veillez à mettre en cache ce nom de fichier s’il est nécessaire à des fins de référence ultérieure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                           | Description                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ suspendue**</dt> </dl> | La capture est dans un état suspendu et doit être arrêtée avant de pouvoir être redémarrée. Appelez [**IDelaydC :: Stop**](idelaydc-stop.md) pour arrêter la capture. Pour plus d’informations, consultez la section Notes de cette rubrique.<br/> |
| <dl> <dt>**\_capture NMERR**</dt> </dl>       | La capture a déjà démarré.<br/>                                                                                                                                                                                 |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>  | Le NPP n’est pas connecté au réseau. appelez [**IDelaydC :: Connecter**](idelaydc-connect.md) pour vous connecter au réseau.<br/>                                                                                          |
| <dl> <dt>**NMERR \_ non \_ retardé**</dt> </dl>    | le NPP est connecté au réseau, mais pas avec la méthode [**IDelaydC :: Connecter**](idelaydc-connect.md) .<br/>                                                                                                      |



 

## <a name="remarks"></a>Remarques

l’emplacement du [*fichier de capture*](c.md) est spécifié dans votre registre Windows, mais vous pouvez utiliser Moniteur réseau pour modifier l’emplacement du fichier.

Pour redémarrer la capture à l’aide de **IDelaydC :: Start** et [**IDelaydC :: Stop**](idelaydc-stop.md), vous devez appeler la méthode [**IDelaydC :: configure**](idelaydc-configure.md) pour reconfigurer la connexion chaque fois que vous appelez la méthode **IDelaydC :: Start** pour redémarrer la capture des données. Lorsque vous démarrez et arrêtez la capture à l’aide de ces trois méthodes, un nouveau fichier de capture est créé chaque fois que la capture est démarrée.

> [!Note]  
> Vous pouvez également démarrer et arrêter la capture à l’aide des méthodes [**IDelaydC ::P ause**](idelaydc-pause.md) et [**IDelaydC :: Resume**](idelaydc-resume.md) . Lorsque vous utilisez ces deux méthodes, les données capturées sont stockées dans le même fichier de capture.

 

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

[**IDelaydC :: configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC :: Connecter**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC ::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC :: Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC :: Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




