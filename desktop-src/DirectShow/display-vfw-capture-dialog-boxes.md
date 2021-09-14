---
description: Afficher les boîtes de dialogue de capture VFW
ms.assetid: 708212ca-d148-4079-8052-3bf6696a33ab
title: Afficher les boîtes de dialogue de capture VFW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b8b51b164630a8fa6e91b2e68ca8a9a3a875b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999663"
---
# <a name="display-vfw-capture-dialog-boxes"></a>Afficher les boîtes de dialogue de capture VFW

un périphérique de capture qui utilise encore un pilote de vidéo pour Windows (VFW) peut prendre en charge les trois boîtes de dialogue suivantes, qui sont utilisées pour configurer l’appareil.



| Boîte de dialogue    | Description                                                                                           |
|---------------|-------------------------------------------------------------------------------------------------------|
| Source vidéo  | Utilisé pour sélectionner l’entrée vidéo et ajuster les paramètres de l’appareil, tels que la luminosité ou le contraste de l’image. |
| Format vidéo  | Utilisé pour sélectionner les dimensions et la profondeur de l’image.                                                    |
| Affichage vidéo | Utilisé pour contrôler l’apparence de la vidéo rendue.                                                 |



 

Pour afficher l’une de ces boîtes de dialogue, procédez comme suit :

1.  Arrêtez le graphique de filtre.
2.  Interrogez le filtre de capture de l’interface [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs) . Si **QueryInterface** se déroule correctement, cela signifie que l’appareil de capture est un appareil VFW.
3.  Appelez [**IAMVfwCaptureDialogs :: HasDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-hasdialog) pour vérifier si le pilote prend en charge la boîte de dialogue que vous souhaitez afficher. L’énumération [**VfwCaptureDialogs**](/windows/desktop/api/strmif/ne-strmif-vfwcapturedialogs) définit des indicateurs pour chacune des boîtes de dialogue VFW. **HasDialog** retourne S \_ OK si la boîte de dialogue est prise en charge. \_Sinon, elle retourne la valeur false. par conséquent, vérifiez la valeur \_ OK directement, plutôt que d’utiliser la macro **Succeeded** .
4.  Si la boîte de dialogue est prise en charge, appelez [**IAMVfwCaptureDialogs :: ShowDialog**](/windows/desktop/api/Strmif/nf-strmif-iamvfwcapturedialogs-showdialog) pour afficher la boîte de dialogue.
5.  Redémarrez le graphique.

Le code suivant illustre ces étapes pour la boîte de dialogue source vidéo :


```C++
pControl->Stop(); // Stop the graph.

// Query the capture filter for the IAMVfwCaptureDialogs interface.
IAMVfwCaptureDialogs *pVfw = 0;
hr = pCap->QueryInterface(IID_IAMVfwCaptureDialogs, (void**)&pVfw);
if (SUCCEEDED(hr))
{
    // Check if the device supports this dialog box.
    if (S_OK == pVfw->HasDialog(VfwCaptureDialog_Source))
    {
        // Show the dialog box.
        hr = pVfw->ShowDialog(VfwCaptureDialog_Source, hwndParent);
    }
}
pControl->Run();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration d’un périphérique de capture vidéo](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



