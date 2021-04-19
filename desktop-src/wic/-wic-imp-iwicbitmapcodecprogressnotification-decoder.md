---
description: Implémentation de IWICBitmapCodecProgressNotification (décodeur)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implémentation de IWICBitmapCodecProgressNotification (décodeur)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534299"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a>Implémentation de IWICBitmapCodecProgressNotification (décodeur)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Lorsqu’un codec effectue une opération d’e/s telle que [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sur une grande image, l’exécution peut prendre plusieurs secondes ou quelques minutes. Lorsque les utilisateurs finaux ne peuvent pas interrompre une opération de longue durée, ils peuvent croire que l’application a été suspendue. Les utilisateurs ferment souvent une application, voire redémarrent leurs ordinateurs, afin de tenter de reprendre le contrôle de leur ordinateur lorsqu’une application ne répond plus.

Cette interface permet à une application de spécifier une fonction de rappel que le codec peut appeler à des intervalles spécifiés pour notifier l’appelant de la progression de l’opération en cours. L’application peut utiliser cette fonction de rappel pour afficher une indication de la progression dans l’interface utilisateur pour notifier l’utilisateur de l’état de l’opération. Si un utilisateur clique sur le bouton **Annuler** de la boîte de dialogue **État d’avancement** , l’application renvoie **WINCODEC \_ Err \_ abandonnée** à partir de la fonction de rappel. Dans ce cas, le codec doit annuler l’opération spécifiée et propager ce **HRESULT** à l’appelant de la méthode qui exécutait l’opération.

Cette interface doit être implémentée sur votre classe de décodeur au niveau du conteneur.


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [RegisterProgressNotification](#registerprogressnotification)
-   [PFNProgressNotification](#pfnprogressnotification)

### <a name="registerprogressnotification"></a>RegisterProgressNotification

[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) est appelé par une application pour inscrire une fonction de rappel que le codec peut appeler à intervalles spécifiés. Le premier paramètre, *pfnProgressNotification*, est un pointeur vers la fonction de rappel que le codec doit appeler à des intervalles réguliers.

Le paramètre *pvData* pointe vers un objet que l’appelant souhaite que le codec renvoie à la fonction de rappel chaque fois que la fonction de rappel est appelée. Cet objet peut être tout et n’a aucune importance particulière pour le codec.

Le paramètre *dwProgressFlags* spécifie quand le codec doit appeler la fonction de rappel. Une fonction ou peut être exécutée avec deux énumérations pour ce paramètre. L’énumération [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) spécifie s’il faut appeler la fonction de rappel pendant le décodage (**WICProgressOperationCopyPixels**), l’encodage (**WICProgerssOperationWritePixels**) ou les deux (**WICProgressOperationAll**).


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



Le codec doit appeler la fonction de rappel à intervalles réguliers tout au long de l’opération, mais l’appelant peut spécifier certaines exigences. L’énumération [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) indique à quel point de l’opération d’appeler la fonction de rappel. Si l’appelant spécifie **WICProgressNotificationBegin**, vous devez l’appeler au début de l’opération (0,0). Si l’appelant ne spécifie pas cela, il est facultatif. De même, si l’appelant spécifie **WICProgerssNotificationEnd**, vous devez l’appeler lorsque l’opération est terminée (1,0). Si l’appelant spécifie **WICProgressNotificationAll**, vous devez l’appeler au début et à la fin, ainsi qu’à intervalles réguliers tout au long de l’opération. L’appelant peut également spécifier **WICProgerssNotificationFrequent**, qui indique qu’il souhaite être rappelé à intervalles fréquents, par exemple après chaque ligne d’analyse. (Un appelant utilise généralement cet indicateur uniquement pour une très grande image.) Dans le cas contraire, vous devez généralement rappeler à intervalles d’environ 10 pour cent du nombre total de lignes de numérisation à traiter.


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



Une seule fonction de rappel à la fois peut être inscrite pour une instance spécifique de décodeur ou d’encodeur. Si une application appelle [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) plusieurs fois, remplacez la fonction de rappel précédemment enregistrée par la nouvelle. Pour annuler une inscription de rappel, un appelant affecte la valeur **null** au paramètre *pfnProgressNotification* .

### <a name="pfnprogressnotification"></a>PFNProgressNotification

[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) est la fonction de rappel avec la signature suivante.


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



Quand vous appelez la fonction de rappel, utilisez le paramètre *pvData* pour retourner le même *pvData* que l’application spécifié lors de l’inscription de la fonction de rappel.

Le paramètre *uFrameNum* doit indiquer l’index du frame en cours de traitement.

Définissez le paramètre d’opération sur **WICProgressOperationCopyPixels** lors du décodage et **WICProgressOperationWritePixels** lors de l’encodage.

Le paramètre *dblProgress* doit être un nombre compris entre 0,0 (le début de l’opération) et 1,0 (la fin de l’opération). La valeur doit refléter la proportion de lignes de numérisation déjà traitées par rapport au nombre total de lignes de numérisation à traiter.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**ProgressNotificationCallback**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Implémentation de IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



