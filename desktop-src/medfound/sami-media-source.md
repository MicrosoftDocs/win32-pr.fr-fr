---
description: Le format SAMI (Synchronized Accessible Media Interchange) est un format permettant d’ajouter des sous-titres à des médias numériques.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: Source du média SAMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7567f7479b6f8d0d2439f89dbf3e6cf273fc7dcae31590ddf9b51a4d66a6940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034817"
---
# <a name="sami-media-source"></a>Source du média SAMI

Le format SAMI (Synchronized Accessible Media Interchange) est un format permettant d’ajouter des sous-titres à des médias numériques. Les légendes sont stockées dans un fichier texte séparé avec l’extension de nom de fichier. SMI ou. sami.

Dans Media Foundation, les fichiers de sous-titres SAMI sont pris en charge par la source du média SAMI. Utilisez le programme de [résolution source](source-resolver.md) pour créer une instance de la source de média sami à partir d’une URL ou d’un flux d’octets. Media Foundation ne fournit pas de composant qui affiche des sous-titres SAMI. L’application doit interpréter les données de sous-titre qu’elle reçoit de la source du média SAMI.

L’exemple suivant montre un exemple de fichier SAMI.

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

L' `<STYLE>` élément contient des informations de style. Cet exemple contient un style de base pour les `<P>` éléments, ainsi que deux styles nommés, « standard » et « Hilite ». Les styles nommés sont utilisés pour modifier le style de base. Les légendes sont placées dans les `<SYNC>` éléments. L’attribut Start donne l’heure de la présentation en millisecondes pour cette légende. Les légendes de cet exemple sont indiquées en deux langues, spécifiées par leurs balises de langue RFC-1766, « en-US » et « fr-FR ». Dans les légendes, les langues sont identifiées par leur nom de classe ; dans ce cas, « ENUSCC » et « FRFRCC ».

La source du média SAMI crée un flux de média pour chaque langue. Par défaut, le premier flux est sélectionné et les flux restants sont désélectionnés. L’application peut modifier la sélection de flux en appelant [**IMFPresentationDescriptor :: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) et [**IMFPresentationDescriptor ::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream). Chaque descripteur de flux contient les attributs suivants.



| Attribut                                                       | Description                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [**\_langage SD \_ MF**](mf-sd-language-attribute.md)            | Balise de langue, comme indiqué par l' `lang` attribut.  |
| [**PP \_ SD \_ ( \_ langage sami)**](mf-sd-sami-language-attribute.md) | Nom de la langue, comme indiqué par l' `Name` attribut. |



 

Chaque flux a le type de média suivant :



| Attribut                                                                            | Valeur                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [**\_type de \_ majeurese MF MT \_**](mf-mt-major-type-attribute.md)                            | **\_Sami MFMediaType** |
| [**MF \_ MT \_ tous les \_ exemples \_ indépendants**](mf-mt-all-samples-independent-attribute.md) | **TRUE**              |



 

La source SAMI remet chaque légende dans un exemple de support séparé. L’horodatage et la durée de l’exemple sont dérivés de l' `<SYNC>` élément. La mémoire tampon de support contenue dans l’exemple contient la légende en tant que texte ASCII. Le style de légende est incorporé dans la légende en tant qu’attribut inline `STYLE` . Par exemple, étant donné le fichier SAMI précédent et l’utilisation du flux en anglais avec les styles par défaut, le premier tampon de média contient les données suivantes. (Les sauts de ligne peuvent différer de ce qui est indiqué ici.)

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a>Styles SAMI

Pour modifier le style actuel, utilisez l’interface [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) . Cette interface est obtenue en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur la source du média sami. (Si vous utilisez la source de média SAMI avec la session multimédia, appelez **GetService** sur la session multimédia.) L’identificateur de service est **le \_ \_ service sami MF**.

L’exemple suivant définit le style SAMI actuel, spécifié par index.


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



Cet exemple appelle les méthodes suivantes sur la source du média SAMI :

-   [**IMFSAMIStyle :: GetStyleCount**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) obtient le nombre de styles.
-   [**IMFSAMIStyle :: GetStyles**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) obtient une liste des noms de style, stockés dans un **PROPVARIANT**.
-   [**IMFSAMIStyle :: SetSelectedStyle**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) définit un style par nom.

La liste des noms de style est également stockée sur le descripteur de présentation, dans l’attribut de STYLELIST de l’attribut [**\_ \_ sami \_ PD**](mf-pd-sami-stylelist-attribute.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sources et récepteurs multimédias](media-sources-and-sinks.md)
</dt> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



