---
description: La méthode SetOneShot spécifie si le filtre d’accrochage de l’exemple s’arrête une fois que le filtre a reçu un exemple.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'ISampleGrabber :: SetOneShot, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006592"
---
# <a name="isamplegrabbersetoneshot-method"></a>ISampleGrabber :: SetOneShot, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La méthode **SetOneShot** spécifie si le filtre d' [**accrochage**](sample-grabber-filter.md) de l’exemple s’arrête une fois que le filtre a reçu un exemple.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OneShot* 
</dt> <dd>

Valeur booléenne qui spécifie si le filtre d’accrochage de l’exemple s’arrête après avoir reçu un échantillon.



| Valeur                                                                                                                                    | Signification                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>VRAI * * * * *</dt> </dl>    | L’exemple d’accrochage s’arrête après le premier échantillon. <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSe * * * * *</dt> </dl> | Après le premier exemple, la méthode d’accrochage continue à traiter les exemples. Il s'agit du comportement par défaut.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Utilisez cette méthode pour obtenir un seul échantillon du flux, comme suit :

1.  Appelez **SetOneShot** avec la valeur **true**.
2.  Vous pouvez également utiliser l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) pour rechercher une position dans le flux.
3.  Appelez [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) pour exécuter le graphique de filtre.
4.  Appelez [**IMediaEvent :: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) pour attendre l’arrêt du graphique. Vous pouvez également appeler [**IMediaEvent :: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) pour obtenir les événements de graphique, jusqu’à ce que vous receviez l’événement [**ce \_ complet**](ec-complete.md) .

Après l’arrêt de la requête d’échantillonnage, le graphique de filtre est toujours en cours d’exécution. Vous pouvez rechercher ou suspendre le graphique pour obtenir un autre exemple.

> [!Note]  
> Une version antérieure de la documentation indiquait que le graphique de filtre s’arrête après la réception de l’exemple. Cela n’est pas exact. Le flux se termine, mais le graphique reste à l’État en cours d’exécution.

 

L’exemple d’accrochage implémente le mode à une seule capture en appelant [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sur le filtre en aval et en renvoyant S \_ false à partir de la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) de ce dernier.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de l’exemple d’accrochage](using-the-sample-grabber.md)
</dt> <dt>

[**Interface ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




