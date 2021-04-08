---
description: Le format SAMI (Synchronized Accessible Media Interchange) est un format permettant d’ajouter des sous-titres à des médias numériques.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: Source du média SAMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9340b51815b130cb41061478358b2ab9dcf68f60
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104042946"
---
# <a name="sami-media-source"></a><span data-ttu-id="c831a-103">Source du média SAMI</span><span class="sxs-lookup"><span data-stu-id="c831a-103">SAMI Media Source</span></span>

<span data-ttu-id="c831a-104">Le format SAMI (Synchronized Accessible Media Interchange) est un format permettant d’ajouter des sous-titres à des médias numériques.</span><span class="sxs-lookup"><span data-stu-id="c831a-104">Synchronized Accessible Media Interchange (SAMI) is a format for adding captions to digital media.</span></span> <span data-ttu-id="c831a-105">Les légendes sont stockées dans un fichier texte séparé avec l’extension de nom de fichier. SMI ou. sami.</span><span class="sxs-lookup"><span data-stu-id="c831a-105">The captions are stored in a separate text file with the file name extension .smi or .sami.</span></span>

<span data-ttu-id="c831a-106">Dans Media Foundation, les fichiers de sous-titres SAMI sont pris en charge par la source du média SAMI.</span><span class="sxs-lookup"><span data-stu-id="c831a-106">In Media Foundation, SAMI caption files are supported through the SAMI media source.</span></span> <span data-ttu-id="c831a-107">Utilisez le programme de [résolution source](source-resolver.md) pour créer une instance de la source de média sami à partir d’une URL ou d’un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="c831a-107">Use the [Source Resolver](source-resolver.md) to create an instance of the SAMI media source from a URL or byte stream.</span></span> <span data-ttu-id="c831a-108">Media Foundation ne fournit pas de composant qui affiche des sous-titres SAMI.</span><span class="sxs-lookup"><span data-stu-id="c831a-108">Media Foundation does not provide a component that displays SAMI captions.</span></span> <span data-ttu-id="c831a-109">L’application doit interpréter les données de sous-titre qu’elle reçoit de la source du média SAMI.</span><span class="sxs-lookup"><span data-stu-id="c831a-109">The application must interpret the caption data that it receives from the SAMI media source.</span></span>

<span data-ttu-id="c831a-110">L’exemple suivant montre un exemple de fichier SAMI.</span><span class="sxs-lookup"><span data-stu-id="c831a-110">The following shows an example SAMI file.</span></span>

``` syntax
<SAMI>
<HEAD>
    <STYLE TYPE="text/css">
    <!--
    P {
        font-family: Arial;
        background: #000000;
        text-align: center;
        }

#standard {Name: Standard; color: #FFFFFF; font-size: 14pt; } 
#hilite {Name: Youth; color: greenyellow; font-size: 18pt;}

    .ENUSCC { Name: English; lang: EN-US-CC; }
    .FRFRCC { Name: French; lang: fr-FR; } 

    -->
    </STYLE>
</HEAD>
<BODY>
    <SYNC Start="0">
        <P Class="ENUSCC">The <I>first</I> caption.</P>
        <P Class="FRFRCC">Un</P>
    </SYNC>
    <SYNC Start="3000">
        <P Class="ENUSCC">The <I>second</I> caption.</P>
        <P Class="FRFRCC">Deux</P>
    </SYNC>
    <SYNC Start="5000">
        <P Class="ENUSCC">The <I>third</I> caption.</P>
        <P Class="FRFRCC">Trois</P>
    </SYNC>
</BODY>
</SAMI>
```

<span data-ttu-id="c831a-111">L' `<STYLE>` élément contient des informations de style.</span><span class="sxs-lookup"><span data-stu-id="c831a-111">The `<STYLE>` element contains style information.</span></span> <span data-ttu-id="c831a-112">Cet exemple contient un style de base pour les `<P>` éléments, ainsi que deux styles nommés, « standard » et « Hilite ».</span><span class="sxs-lookup"><span data-stu-id="c831a-112">This example contains a base style for `<P>` elements, along with two named styles, "standard" and "hilite".</span></span> <span data-ttu-id="c831a-113">Les styles nommés sont utilisés pour modifier le style de base.</span><span class="sxs-lookup"><span data-stu-id="c831a-113">The named styles are used to modify the base style.</span></span> <span data-ttu-id="c831a-114">Les légendes sont placées dans les `<SYNC>` éléments.</span><span class="sxs-lookup"><span data-stu-id="c831a-114">Captions are placed within `<SYNC>` elements.</span></span> <span data-ttu-id="c831a-115">L’attribut Start donne l’heure de la présentation en millisecondes pour cette légende.</span><span class="sxs-lookup"><span data-stu-id="c831a-115">The start attribute gives the presentation time in milliseconds for that caption.</span></span> <span data-ttu-id="c831a-116">Les légendes de cet exemple sont indiquées en deux langues, spécifiées par leurs balises de langue RFC-1766, « en-US » et « fr-FR ».</span><span class="sxs-lookup"><span data-stu-id="c831a-116">The captions in this example are given in two languages, specified by their RFC-1766 language tags, "en-US" and "fr -FR".</span></span> <span data-ttu-id="c831a-117">Dans les légendes, les langues sont identifiées par leur nom de classe ; dans ce cas, « ENUSCC » et « FRFRCC ».</span><span class="sxs-lookup"><span data-stu-id="c831a-117">Within the captions, languages are identified by their class names; in this case, "ENUSCC" and "FRFRCC".</span></span>

<span data-ttu-id="c831a-118">La source du média SAMI crée un flux de média pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="c831a-118">The SAMI media source creates one media stream for each language.</span></span> <span data-ttu-id="c831a-119">Par défaut, le premier flux est sélectionné et les flux restants sont désélectionnés.</span><span class="sxs-lookup"><span data-stu-id="c831a-119">By default, the first stream is selected and the remaining streams are deselected.</span></span> <span data-ttu-id="c831a-120">L’application peut modifier la sélection de flux en appelant [**IMFPresentationDescriptor :: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) et [**IMFPresentationDescriptor ::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="c831a-120">The application can change the stream selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span> <span data-ttu-id="c831a-121">Chaque descripteur de flux contient les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="c831a-121">Each stream descriptor contains the following attributes.</span></span>



| <span data-ttu-id="c831a-122">Attribut</span><span class="sxs-lookup"><span data-stu-id="c831a-122">Attribute</span></span>                                                       | <span data-ttu-id="c831a-123">Description</span><span class="sxs-lookup"><span data-stu-id="c831a-123">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="c831a-124">**\_langage SD \_ MF**</span><span class="sxs-lookup"><span data-stu-id="c831a-124">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)            | <span data-ttu-id="c831a-125">Balise de langue, comme indiqué par l' `lang` attribut.</span><span class="sxs-lookup"><span data-stu-id="c831a-125">Language tag, as given by the `lang` attribute.</span></span>  |
| [<span data-ttu-id="c831a-126">**PP \_ SD \_ ( \_ langage sami)**</span><span class="sxs-lookup"><span data-stu-id="c831a-126">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="c831a-127">Nom de la langue, comme indiqué par l' `Name` attribut.</span><span class="sxs-lookup"><span data-stu-id="c831a-127">Language name, as given by the `Name` attribute.</span></span> |



 

<span data-ttu-id="c831a-128">Chaque flux a le type de média suivant :</span><span class="sxs-lookup"><span data-stu-id="c831a-128">Each stream has the following media type:</span></span>



| <span data-ttu-id="c831a-129">Attribut</span><span class="sxs-lookup"><span data-stu-id="c831a-129">Attribute</span></span>                                                                            | <span data-ttu-id="c831a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="c831a-130">Value</span></span>                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [<span data-ttu-id="c831a-131">**\_type de \_ majeurese MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="c831a-131">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                            | <span data-ttu-id="c831a-132">**\_Sami MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c831a-132">**MFMediaType\_SAMI**</span></span> |
| [<span data-ttu-id="c831a-133">**MF \_ MT \_ tous les \_ exemples \_ indépendants**</span><span class="sxs-lookup"><span data-stu-id="c831a-133">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) | <span data-ttu-id="c831a-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c831a-134">**TRUE**</span></span>              |



 

<span data-ttu-id="c831a-135">La source SAMI remet chaque légende dans un exemple de support séparé.</span><span class="sxs-lookup"><span data-stu-id="c831a-135">The SAMI source delivers each caption in a separate media sample.</span></span> <span data-ttu-id="c831a-136">L’horodatage et la durée de l’exemple sont dérivés de l' `<SYNC>` élément.</span><span class="sxs-lookup"><span data-stu-id="c831a-136">The sample time stamp and duration are derived from the `<SYNC>` element.</span></span> <span data-ttu-id="c831a-137">La mémoire tampon de support contenue dans l’exemple contient la légende en tant que texte ASCII.</span><span class="sxs-lookup"><span data-stu-id="c831a-137">The media buffer contained in the sample holds the caption as ASCII text.</span></span> <span data-ttu-id="c831a-138">Le style de légende est incorporé dans la légende en tant qu’attribut inline `STYLE` .</span><span class="sxs-lookup"><span data-stu-id="c831a-138">The caption style is embedded in the caption as an inline `STYLE` attribute.</span></span> <span data-ttu-id="c831a-139">Par exemple, étant donné le fichier SAMI précédent et l’utilisation du flux en anglais avec les styles par défaut, le premier tampon de média contient les données suivantes.</span><span class="sxs-lookup"><span data-stu-id="c831a-139">For example, given the previous SAMI file, and using the English-language stream with the default styles, the first media buffer would contain the following data.</span></span> <span data-ttu-id="c831a-140">(Les sauts de ligne peuvent différer de ce qui est indiqué ici.)</span><span class="sxs-lookup"><span data-stu-id="c831a-140">(The line breaks might differ from what is shown here.)</span></span>

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a><span data-ttu-id="c831a-141">Styles SAMI</span><span class="sxs-lookup"><span data-stu-id="c831a-141">SAMI Styles</span></span>

<span data-ttu-id="c831a-142">Pour modifier le style actuel, utilisez l’interface [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .</span><span class="sxs-lookup"><span data-stu-id="c831a-142">To change the current style, use the [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) interface.</span></span> <span data-ttu-id="c831a-143">Cette interface est obtenue en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur la source du média sami.</span><span class="sxs-lookup"><span data-stu-id="c831a-143">This interface is obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the SAMI media source.</span></span> <span data-ttu-id="c831a-144">(Si vous utilisez la source de média SAMI avec la session multimédia, appelez **GetService** sur la session multimédia.) L’identificateur de service est **le \_ \_ service sami MF**.</span><span class="sxs-lookup"><span data-stu-id="c831a-144">(If you are using the SAMI media source with the Media Session, call **GetService** on the Media Session.) The service identifier is **MF\_SAMI\_SERVICE**.</span></span>

<span data-ttu-id="c831a-145">L’exemple suivant définit le style SAMI actuel, spécifié par index.</span><span class="sxs-lookup"><span data-stu-id="c831a-145">The following example sets the current SAMI style, specified by index.</span></span>


```C++
HRESULT SetSAMIStyleByIndex(IMFMediaSource *pSource, DWORD index)
{
    IMFSAMIStyle *pSami = NULL;

    DWORD cStyles;
    PROPVARIANT varStyles;

    HRESULT hr = MFGetService(pSource, MF_SAMI_SERVICE, IID_PPV_ARGS(&pSami));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->GetStyleCount(&cStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    if (index >= cStyles)
    {
        hr = E_INVALIDARG;
        goto done;
    }

    hr = pSami->GetStyles(&varStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->SetSelectedStyle(varStyles.calpwstr.pElems[index]);

done:
    PropVariantClear(&varStyles);
    SafeRelease(&pSami);
    return hr;
}
```



<span data-ttu-id="c831a-146">Cet exemple appelle les méthodes suivantes sur la source du média SAMI :</span><span class="sxs-lookup"><span data-stu-id="c831a-146">This example calls the following methods on the SAMI media source:</span></span>

-   <span data-ttu-id="c831a-147">[**IMFSAMIStyle :: GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) obtient le nombre de styles.</span><span class="sxs-lookup"><span data-stu-id="c831a-147">[**IMFSAMIStyle::GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) gets the number of styles.</span></span>
-   <span data-ttu-id="c831a-148">[**IMFSAMIStyle :: GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) obtient une liste des noms de style, stockés dans un **PROPVARIANT**.</span><span class="sxs-lookup"><span data-stu-id="c831a-148">[**IMFSAMIStyle::GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) gets a list of the style names, stored in a **PROPVARIANT**.</span></span>
-   <span data-ttu-id="c831a-149">[**IMFSAMIStyle :: SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) définit un style par nom.</span><span class="sxs-lookup"><span data-stu-id="c831a-149">[**IMFSAMIStyle::SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) sets a style by name.</span></span>

<span data-ttu-id="c831a-150">La liste des noms de style est également stockée sur le descripteur de présentation, dans l’attribut de STYLELIST de l’attribut [**\_ \_ sami \_ PD**](mf-pd-sami-stylelist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c831a-150">The list of style names is also stored on the presentation descriptor, in the [**MF\_PD\_SAMI\_STYLELIST**](mf-pd-sami-stylelist-attribute.md) attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c831a-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c831a-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c831a-152">Sources et récepteurs multimédias</span><span class="sxs-lookup"><span data-stu-id="c831a-152">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="c831a-153">Formats multimédias pris en charge dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c831a-153">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



