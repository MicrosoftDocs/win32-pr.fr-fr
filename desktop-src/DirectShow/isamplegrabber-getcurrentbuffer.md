---
description: La méthode GetCurrentBuffer récupère une copie de la mémoire tampon associée à l’exemple le plus récent.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'ISampleGrabber :: GetCurrentBuffer, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857493"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a>ISampleGrabber :: GetCurrentBuffer, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La méthode **GetCurrentBuffer** récupère une copie de la mémoire tampon associée à l’exemple le plus récent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBufferSize* \[ in, out\]
</dt> <dd>

Pointeur vers la taille de la mémoire tampon. Si *pbuffer* a la **valeur null**, ce paramètre reçoit la taille de mémoire tampon requise, en octets. Si *pbuffer* n’a pas la **valeur null**, définissez ce paramètre sur la taille de la mémoire tampon, en octets. Lors de la sortie, le paramètre reçoit le nombre d’octets qui ont été copiés dans la mémoire tampon. Cette valeur peut être inférieure à la taille de la mémoire tampon.

</dd> <dt>

*pbuffer* \[ à\]
</dt> <dd>

Pointeur vers un tableau d’octets de taille *pBufferSize* ou **null**. Si ce paramètre n’est pas **null**, la mémoire tampon en cours est copiée dans le tableau. Si ce paramètre a la **valeur null**, le paramètre *pBufferSize* reçoit la taille de mémoire tampon requise.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs suivantes.



| Code de retour                                                                                           | Description                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Les exemples ne sont pas mis en mémoire tampon. Appelez [**ISampleGrabber :: SetBufferSamples**](isamplegrabber-setbuffersamples.md).<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>         | La mémoire tampon spécifiée n’est pas assez grande.<br/>                                                                         |
| <dl> <dt>**\_pointeur E**</dt> </dl>             | Argument de pointeur **null** .<br/>                                                                                        |
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                                                                                                          |
| <dl> <dt>**VFW \_ E \_ non \_ connecté**</dt> </dl> | Le filtre n’est pas connecté.<br/>                                                                                      |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl>   | Le filtre n’a pas encore reçu d’exemples. Pour remettre un exemple, exécutez ou suspendez le graphique.<br/>                         |



 

## <a name="remarks"></a>Notes

Pour activer la mise en mémoire tampon, appelez [**ISampleGrabber :: SetBufferSamples**](isamplegrabber-setbuffersamples.md) avec la valeur **true**.

Appelez cette méthode deux fois. Lors du premier appel, affectez à *pbuffer* la **valeur null**. La taille de la mémoire tampon est retournée dans *pBufferSize*. Allouez ensuite un tableau et rappelez la méthode. Lors du deuxième appel, transmettez la taille du tableau dans *pBufferSize* et transmettez l’adresse du tableau dans *pbuffer*. Si le tableau n’est pas assez grand, la méthode retourne E \_ OUTOFMEMORY.

Le paramètre *pbuffer* est typé comme pointeur **long** , mais le contenu de la mémoire tampon dépend du format des données. Appelez [**ISampleGrabber :: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) pour accéder au type de média du format.

N’appelez pas cette méthode pendant que le graphique de filtre est en cours d’exécution. Lorsque le graphique de filtre est en cours d’exécution, le filtre d’accrochage remplace le contenu de la mémoire tampon à chaque fois qu’il reçoit un nouvel exemple. La meilleure façon d’utiliser cette méthode consiste à utiliser le « mode à une seule capture », qui arrête le graphique après avoir reçu le premier exemple. Pour définir le mode d’une seule capture, appelez [**ISampleGrabber :: SetOneShot**](isamplegrabber-setoneshot.md).

Le filtre ne met pas en mémoire tampon des exemples de préroll, ou des exemples dans lesquels le membre **dwStreamId** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) est autre chose que le \_ média de flux \_ .

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

 

 




