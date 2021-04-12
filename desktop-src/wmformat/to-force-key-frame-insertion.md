---
title: Pour forcer l’insertion d' Key-Frame
description: Pour forcer l’insertion d' Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- ASF (Advanced Systems Format), forçage des insertions de trame clé
- ASF (format de systèmes avancés), forcer les insertions de trame clé
- ASF (Advanced Systems Format), insertions d’image clé
- ASF (format des systèmes avancés), insertions d’image clé
- images clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104462782"
---
# <a name="to-force-key-frame-insertion"></a><span data-ttu-id="3db5d-108">Pour forcer l’insertion d' Key-Frame</span><span class="sxs-lookup"><span data-stu-id="3db5d-108">To Force Key-Frame Insertion</span></span>

<span data-ttu-id="3db5d-109">Le codec Windows Media Video 9 prend en charge l’insertion d’image clé forcée.</span><span class="sxs-lookup"><span data-stu-id="3db5d-109">The Windows Media Video 9 codec supports forced key-frame insertion.</span></span> <span data-ttu-id="3db5d-110">Lorsque vous transmettez un exemple au writer, vous pouvez spécifier qu’il doit être encodé sous la forme d’une [*image clé*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="3db5d-110">When you pass a sample to the writer, you can specify that it must be encoded as a [*key frame*](wmformat-glossary.md).</span></span>

<span data-ttu-id="3db5d-111">Pour forcer l’insertion d’une image clé pour un exemple, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="3db5d-111">To force key-frame insertion for a sample, perform the following steps.</span></span>

1.  <span data-ttu-id="3db5d-112">Allouez une mémoire tampon pour contenir l’exemple et récupérez un pointeur vers l’interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) contenant la mémoire tampon en appelant [**IWMWriter :: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span><span class="sxs-lookup"><span data-stu-id="3db5d-112">Allocate a buffer to hold the sample, and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface containing the buffer by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="3db5d-113">Récupérez l’emplacement et la taille de la mémoire tampon créée à l’étape 1 en appelant [**INSSBuffer :: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span><span class="sxs-lookup"><span data-stu-id="3db5d-113">Retrieve the location and size of the buffer created in step 1 by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span></span>
3.  <span data-ttu-id="3db5d-114">Copiez vos données d’exemple dans l’emplacement de la mémoire tampon, en vous assurant que l’exemple passé sera contenu dans la mémoire tampon allouée.</span><span class="sxs-lookup"><span data-stu-id="3db5d-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="3db5d-115">En fonction de la source de vos exemples, vous pouvez utiliser diverses fonctions pour copier les données.</span><span class="sxs-lookup"><span data-stu-id="3db5d-115">Depending upon the source of your samples, you can use a variety of functions to copy the data.</span></span> <span data-ttu-id="3db5d-116">Par exemple, si vous copiez un flux à partir d’un fichier AVI, vous pouvez utiliser la fonction AVI, **AVIStreamRead**.</span><span class="sxs-lookup"><span data-stu-id="3db5d-116">For example, if you are copying a stream from an AVI file, you can use the AVI function, **AVIStreamRead**.</span></span>
4.  <span data-ttu-id="3db5d-117">Mettez à jour la quantité de données utilisées dans la mémoire tampon pour refléter la taille réelle de l’exemple en appelant [**INSSBuffer :: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span><span class="sxs-lookup"><span data-stu-id="3db5d-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="3db5d-118">Obtenez un pointeur vers l’interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) en appelant **INSSBuffer :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="3db5d-118">Obtain a pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface by calling **INSSBuffer::QueryInterface**.</span></span>
6.  <span data-ttu-id="3db5d-119">Définissez l’exemple comme une image clé forcée en appelant la méthode [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) pour définir la \_ propriété WM SampleExtensionGUID \_ OutputCleanPoint.</span><span class="sxs-lookup"><span data-stu-id="3db5d-119">Set the sample as a forced key frame by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the WM\_SampleExtensionGUID\_OutputCleanPoint property.</span></span> <span data-ttu-id="3db5d-120">Cette propriété est une valeur booléenne ; Affectez-lui la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="3db5d-120">This property is a Boolean value; set it to **TRUE**.</span></span>
7.  <span data-ttu-id="3db5d-121">Transmettez l’interface de mémoire tampon à l’enregistreur avec le nombre d’entrées et l’heure d’échantillonnage à l’aide de la méthode [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="3db5d-121">Pass the buffer interface to the writer along with the input number and sample time by using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3db5d-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3db5d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3db5d-123">**IWMWriter::WriteSample**</span><span class="sxs-lookup"><span data-stu-id="3db5d-123">**IWMWriter::WriteSample**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[<span data-ttu-id="3db5d-124">**Pour écrire des exemples**</span><span class="sxs-lookup"><span data-stu-id="3db5d-124">**To Write Samples**</span></span>](to-write-samples.md)
</dt> <dt>

[<span data-ttu-id="3db5d-125">**Encodage à vitesse de transmission variable (VBR)**</span><span class="sxs-lookup"><span data-stu-id="3db5d-125">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="3db5d-126">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="3db5d-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




