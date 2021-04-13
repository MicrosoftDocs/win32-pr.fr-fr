---
title: Pour récupérer des exemples de médias avec le lecteur synchrone
description: Pour récupérer des exemples de médias avec le lecteur synchrone
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- ASF (Advanced Systems Format), récupération des exemples de supports
- ASF (format des systèmes avancés), récupération des exemples de média
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- lecteurs synchrones, récupération d’exemples de médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381510"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a>Pour récupérer des exemples de médias avec le lecteur synchrone

Vous devez demander chaque exemple l’un après l’autre à partir du lecteur synchrone. Vous bénéficiez ainsi d’un plus grand contrôle sur les exemples que vous recevez et le moment où vous les recevez.

Utilisez la méthode [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) pour récupérer un exemple. Vous devez passer principalement des pointeurs vers des variables qui seront remplies avec des informations sur l’exemple récupéré en tant que paramètres. Le seul paramètre d’entrée est *wStreamNum*. Si vous transmettez un numéro de flux, **GetNextSample** récupère l’échantillon suivant avec le numéro de flux spécifié. Si vous transmettez zéro pour *wStreamNum*, l’exemple suivant qui se produit chronologiquement dans le fichier est récupéré.

Par défaut, le lecteur synchrone récupère tous les échantillons des sorties d’un fichier dans l’ordre chronologique. Si vous appelez **GetNextSample** et qu’il n’y a plus d’exemples à obtenir, il retournera NS \_ E \_ no \_ More \_ , qui est un code d’erreur qui a échoué. Lors du codage par conséquent, vous pouvez simplement parcourir les exemples jusqu’à ce que la méthode échoue.

> [!Note]  
> Pour vous assurer que le lecteur synchrone fournit des durées d’échantillonnage correctes pour les flux vidéo, vous devez d’abord configurer la sortie du flux. Appelez la méthode [**IWMSyncReader :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) pour définir le \_ paramètre g wszVideoSampleDurations sur **true**.

 

Exemple de code

L’exemple de code suivant montre comment utiliser **GetNextSample** pour récupérer tous les exemples d’un fichier.


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




