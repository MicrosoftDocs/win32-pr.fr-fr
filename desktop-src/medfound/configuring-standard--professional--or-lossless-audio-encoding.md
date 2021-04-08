---
description: Lorsque l’encodeur Windows Media Audio énumère les types de sortie, il identifie chaque type énuméré comme standard, Professional ou Lossless.
ms.assetid: 1c3d22c3-10f7-454a-b1c1-372d684b6568
title: Configuration de l’encodage audio standard, Professional ou Lossless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e781c2c093b46a12fa4ad5434f97931a948ff9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749333"
---
# <a name="configuring-standard-professional-or-lossless-audio-encoding"></a><span data-ttu-id="14f83-103">Configuration de l’encodage audio standard, Professional ou Lossless</span><span class="sxs-lookup"><span data-stu-id="14f83-103">Configuring Standard, Professional, or Lossless Audio Encoding</span></span>

<span data-ttu-id="14f83-104">Lorsque l’encodeur Windows Media Audio énumère les types de sortie, il identifie chaque type énuméré comme standard, Professional ou Lossless.</span><span class="sxs-lookup"><span data-stu-id="14f83-104">When the Windows Media Audio encoder enumerates output types, it identifies each enumerated type as either Standard, Professional, or Lossless.</span></span> <span data-ttu-id="14f83-105">Vous pouvez déterminer si un type de sortie est standard, Professional ou Lossless en effectuant les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="14f83-105">You can determine whether an output type is Standard, Professional, or Lossless by performing the following steps.</span></span>

1.  <span data-ttu-id="14f83-106">Appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour obtenir une interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) qui représente le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="14f83-106">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to obtain an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface that represents the output type.</span></span>
2.  <span data-ttu-id="14f83-107">Appelez [**IMFMediaType :: GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) pour obtenir une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui contient des informations sur le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="14f83-107">Call [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation) to get an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains information about the output type.</span></span>
3.  <span data-ttu-id="14f83-108">Le membre **pbFormat** de la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) pointe vers une structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) qui contient des informations supplémentaires sur le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="14f83-108">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure points to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure that contains additional information about the output type.</span></span> <span data-ttu-id="14f83-109">Inspectez le membre **wFormatTag** de la structure **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="14f83-109">Inspect the **wFormatTag** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="14f83-110">La valeur 0x161 indique standard, la valeur 0x162 indique Professional et la valeur 0x163 indique Lossless.</span><span class="sxs-lookup"><span data-stu-id="14f83-110">A value of 0x161 indicates Standard, a value of 0x162 indicates Professional, and a value of 0x163 indicates Lossless.</span></span>

<span data-ttu-id="14f83-111">Si vous définissez des propriétés sur l’encodeur Windows Media Audio avant d’énumérer les types de sortie, vous pouvez limiter le nombre de types de sortie énumérés.</span><span class="sxs-lookup"><span data-stu-id="14f83-111">If you set properties on the Windows Media Audio encoder before you enumerate output types, you can limit the number of output types that are enumerated.</span></span> <span data-ttu-id="14f83-112">Par exemple, si vous définissez les propriétés VBR de manière appropriée, vous pouvez limiter les types de sortie énumérés à ceux qui se trouvent dans la catégorie sans perte.</span><span class="sxs-lookup"><span data-stu-id="14f83-112">For example, if you set the VBR properties appropriately, you can limit the enumerated output types to those that are in the Lossless category.</span></span>

## <a name="standard-audio-encoding"></a><span data-ttu-id="14f83-113">Encodage audio standard</span><span class="sxs-lookup"><span data-stu-id="14f83-113">Standard Audio Encoding</span></span>

<span data-ttu-id="14f83-114">Vous pouvez utiliser les étapes suivantes pour configurer l’encodage audio standard.</span><span class="sxs-lookup"><span data-stu-id="14f83-114">You can use the following steps to configure Standard audio encoding.</span></span>

1.  <span data-ttu-id="14f83-115">Définissez les propriétés de votre choix sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="14f83-115">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="14f83-116">Énumérer les types de sortie possibles.</span><span class="sxs-lookup"><span data-stu-id="14f83-116">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="14f83-117">Inspectez les types énumérés et choisissez celui qui a une balise de format audio 0x161.</span><span class="sxs-lookup"><span data-stu-id="14f83-117">Inspect the enumerated types and choose one that has an audio format tag of 0x161.</span></span>
4.  <span data-ttu-id="14f83-118">Définissez le type de sortie sur le type choisi en appelant [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="14f83-118">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="professional-audio-encoding"></a><span data-ttu-id="14f83-119">Encodage audio professionnel</span><span class="sxs-lookup"><span data-stu-id="14f83-119">Professional Audio Encoding</span></span>

<span data-ttu-id="14f83-120">Vous pouvez utiliser les étapes suivantes pour configurer l’encodage audio professionnel.</span><span class="sxs-lookup"><span data-stu-id="14f83-120">You can use the following steps to configure Professional audio encoding.</span></span>

1.  <span data-ttu-id="14f83-121">Définissez les propriétés de votre choix sur l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="14f83-121">Set the properties of your choice on the encoder.</span></span>
2.  <span data-ttu-id="14f83-122">Énumérer les types de sortie possibles.</span><span class="sxs-lookup"><span data-stu-id="14f83-122">Enumerate the possible output types.</span></span>
3.  <span data-ttu-id="14f83-123">Inspectez les types énumérés et choisissez celui qui a une balise de format audio 0x162.</span><span class="sxs-lookup"><span data-stu-id="14f83-123">Inspect the enumerated types and choose one that has an audio format tag of 0x162.</span></span>
4.  <span data-ttu-id="14f83-124">Définissez le type de sortie sur le type choisi en appelant [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="14f83-124">Set the output type to your chosen type by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="lossless-audio-encoding"></a><span data-ttu-id="14f83-125">Encodage audio sans perte</span><span class="sxs-lookup"><span data-stu-id="14f83-125">Lossless Audio Encoding</span></span>

<span data-ttu-id="14f83-126">Vous pouvez utiliser les étapes suivantes pour configurer l’encodage audio sans perte.</span><span class="sxs-lookup"><span data-stu-id="14f83-126">You can use the following steps to configure Lossless audio encoding.</span></span>

1.  <span data-ttu-id="14f83-127">Affectez à la propriété [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) la **\_ valeur variant true**.</span><span class="sxs-lookup"><span data-stu-id="14f83-127">Set the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to **VARIANT\_TRUE**.</span></span>
2.  <span data-ttu-id="14f83-128">Affectez à la propriété MFPKEY de la [**\_ contrainte \_ énumérée \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) la **\_ valeur variant true**.</span><span class="sxs-lookup"><span data-stu-id="14f83-128">Set the [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) property to **VARIANT\_TRUE**.</span></span>
3.  <span data-ttu-id="14f83-129">Définissez la propriété [**MFPKEY \_ souhaitée \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) sur 100.</span><span class="sxs-lookup"><span data-stu-id="14f83-129">Set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property to 100.</span></span>
4.  <span data-ttu-id="14f83-130">Énumérer les types de sortie.</span><span class="sxs-lookup"><span data-stu-id="14f83-130">Enumerate output types.</span></span>
5.  <span data-ttu-id="14f83-131">Définissez le type de sortie sur l’un des types énumérés à l’étape 4 en appelant [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="14f83-131">Set the output type to one of the types enumerated in step 4 by calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="14f83-132">Le code suivant énumère tous les types de sortie sans perte pour l’encodeur Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="14f83-132">The following code enumerates all of the lossless output types for the Windows Media Audio encoder.</span></span> <span data-ttu-id="14f83-133">Le code imprime la valeur de la balise de format audio pour chaque type énuméré.</span><span class="sxs-lookup"><span data-stu-id="14f83-133">The code prints the value of the audio format tag for each enumerated type.</span></span> <span data-ttu-id="14f83-134">Étant donné que tous les types énumérés sont sans perte, toutes ces balises de mise en forme ont la valeur 0x163.</span><span class="sxs-lookup"><span data-stu-id="14f83-134">Because all of the enumerated types are lossless, all of those format tags have a value of 0x163.</span></span> <span data-ttu-id="14f83-135">Supposons que pIMT est un pointeur vers une interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) sur un objet encodeur Windows Media audio et que pStore est un pointeur vers une interface **IPropertyStore** sur le même objet.</span><span class="sxs-lookup"><span data-stu-id="14f83-135">Assume that pIMT is a pointer to an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a Windows Media Audio encoder object and that pStore is a pointer to an **IPropertyStore** interface on the same object.</span></span> <span data-ttu-id="14f83-136">Supposons également que HR est une variable de type **HRESULT** qui a été déclarée précédemment dans le code.</span><span class="sxs-lookup"><span data-stu-id="14f83-136">Also assume that hr is a variable of type **HRESULT** that was declared previously in the code.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="14f83-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14f83-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14f83-138">Configuration de l’encodage audio</span><span class="sxs-lookup"><span data-stu-id="14f83-138">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> </dl>

 

 
