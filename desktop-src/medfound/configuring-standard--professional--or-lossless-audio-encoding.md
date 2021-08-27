---
description: lorsque l’encodeur Windows Media Audio énumère les types de sortie, il identifie chaque type énuméré comme Standard, Professional ou Lossless.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: configuration de l’encodage Audio Standard, Professional ou sans perte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa4184af8bc6b83710a3710ac1a278de71de0b7221dc11757bdeba46af8c7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743536"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a>configuration de l’encodage Audio Standard, Professional ou sans perte

lorsque l’encodeur Windows Media Audio énumère les types de sortie, il identifie chaque type énuméré comme Standard, Professional ou Lossless. vous pouvez déterminer si un type de sortie est Standard, Professional ou sans perte en effectuant les étapes suivantes.

1.  Appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour obtenir une interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) qui représente le type de sortie.
2.  Appelez [**IMFMediaType :: GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) pour obtenir une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui contient des informations sur le type de sortie.
3.  Le membre **pbFormat** de la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) pointe vers une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) qui contient des informations supplémentaires sur le type de sortie. Inspectez le membre **wFormatTag** de la structure **WAVEFORMATEX** . la valeur 0x161 indique Standard, la valeur 0x162 indique Professional et la valeur 0x163 indique Lossless.

si vous définissez des propriétés sur l’encodeur Windows Media Audio avant d’énumérer les types de sortie, vous pouvez limiter le nombre de types de sortie énumérés. Par exemple, si vous définissez les propriétés VBR de manière appropriée, vous pouvez limiter les types de sortie énumérés à ceux qui se trouvent dans la catégorie sans perte.

## <a name="standard-audio-encoding"></a>Encodage audio standard

Vous pouvez utiliser les étapes suivantes pour configurer l’encodage audio standard.

1.  Définissez les propriétés de votre choix sur l’encodeur.
2.  Énumérer les types de sortie possibles.
3.  Inspectez les types énumérés et choisissez celui qui a une balise de format audio 0x161.
4.  Définissez le type de sortie sur le type choisi en appelant [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="professional-audio-encoding"></a>Professional Encodage audio

vous pouvez utiliser les étapes suivantes pour configurer Professional l’encodage audio.

1.  Définissez les propriétés de votre choix sur l’encodeur.
2.  Énumérer les types de sortie possibles.
3.  Inspectez les types énumérés et choisissez celui qui a une balise de format audio 0x162.
4.  Définissez le type de sortie sur le type choisi en appelant [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="lossless-audio-encoding"></a>Encodage audio sans perte

Vous pouvez utiliser les étapes suivantes pour configurer l’encodage audio sans perte.

1.  Affectez à la propriété [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) la **\_ valeur variant true**.
2.  Affectez à la propriété MFPKEY de la [**\_ contrainte \_ énumérée \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) la **\_ valeur variant true**.
3.  Définissez la propriété [**MFPKEY \_ souhaitée \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) sur 100.
4.  Énumérer les types de sortie.
5.  Définissez le type de sortie sur l’un des types énumérés à l’étape 4 en appelant [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

le code suivant énumère tous les types de sortie sans perte pour l’encodeur Windows Media Audio. Le code imprime la valeur de la balise de format audio pour chaque type énuméré. Étant donné que tous les types énumérés sont sans perte, toutes ces balises de mise en forme ont la valeur 0x163. supposons que pIMT est un pointeur vers une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un objet encodeur Windows Media Audio et que pStore est un pointeur vers une interface **IPropertyStore** sur le même objet. Supposons également que HR est une variable de type **HRESULT** qui a été déclarée précédemment dans le code.


```
PROPVARIANT prop;
prop.vt = VT_BOOL;
prop.boolVal = VARIANT_TRUE;
hr = pStore->SetValue(MFPKEY_VBRENABLED, prop);

if(SUCCEEDED(hr))
{
   hr = pStore->SetValue(MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY, prop);

   if(SUCCEEDED(hr))
   {
      prop.vt = VT_UI4;
      prop.ulVal = 100;
      hr = pStore->SetValue(MFPKEY_DESIRED_VBRQUALITY, prop);
      
      if(SUCCEEDED(hr))
      {           
         HRESULT hrAvailableType = S_OK;
         LONG j = 0;
         while(MF_E_NO_MORE_TYPES != hrAvailableType)
         {
            IMFMediaType* pOutputType = NULL;     
            hrAvailableType = pIMFT->GetOutputAvailableType(
               0, j, &pOutputType);

            if(SUCCEEDED(hrAvailableType))
            {
               AM_MEDIA_TYPE* pTypeRep = NULL;
               hr = pOutputType->GetRepresentation(
                  AM_MEDIA_TYPE_REPRESENTATION, (VOID**)&pTypeRep); 
                     
               if(SUCCEEDED(hr))
               {
                  WAVEFORMATEX* pwfex = (WAVEFORMATEX*)pTypeRep->pbFormat;
                  printf_s("%x\n", pwfex->wFormatTag);
                  pOutputType->FreeRepresentation(
                     AM_MEDIA_TYPE_REPRESENTATION, (VOID*)pTypeRep);
               }

               pOutputType->Release();
               ++j;
            }                                                                  
         } // while                 
      }                                
   } 
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’encodage audio](configuringaudioencoding.md)
</dt> </dl>

 

 
