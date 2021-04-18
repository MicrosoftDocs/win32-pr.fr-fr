---
description: Génération d’un nouvel objet d’en-tête ASF
ms.assetid: cf73306d-156a-45c0-a3d6-ae48734f5709
title: Génération d’un nouvel objet d’en-tête ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f303be4eb3353a0e7ddf1dad0eff9956f68d7db5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524511"
---
# <a name="generating-a-new-asf-header-object"></a>Génération d’un nouvel objet d’en-tête ASF

Pour convertir les informations contenues dans l’objet ContentInfo en un format d’objet d’en-tête ASF binaire, l’application doit appeler [**IMFASFContentInfo :: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Cet appel doit être effectué après la génération des paquets de données et l’objet ContentInfo contient des informations mises à jour. **GenerateHeader** retourne un pointeur vers une mémoire tampon de média qui contient les informations d’en-tête dans le format valide. L’application peut ensuite écrire les données, pointées par la mémoire tampon du média, au début d’un nouveau fichier ASF.

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a>Pour écrire un nouvel objet d’en-tête à l’aide de l’objet ContentInfo

1.  Appelez [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) pour créer un objet ContentInfo vide.
2.  Appelez [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) pour fournir l’objet de profil à l’objet ContentInfo. Pour plus d’informations sur la création de profils, consultez [création d’un profil ASF](creating-an-asf-profile.md).
3.  Appelez [**IMFASFContentInfo :: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) et transmettez **null** dans le paramètre *pIHeader* et recevez la taille de l’objet ContentInfo rempli dans le paramètre *pcbHeader* . L’application peut utiliser cette valeur pour allouer de la mémoire ou la mémoire tampon du média qui contiendra l’objet d’en-tête.

    La taille d’en-tête reçue comprend la taille de remplissage, qui est ajustée en fonction de la taille réelle des objets d’en-tête. La taille maximale des objets d’en-tête est de 10 Mo. Si la taille dépasse cette valeur, **GenerateHeader** échoue avec l' \_ erreur MF E \_ ASF \_ sera déplacé.

4.  Appelez [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) pour créer une mémoire tampon de média de la taille reçue à l’étape 3.
5.  Appelez à nouveau **GenerateHeader** pour générer le nouvel objet d’en-tête ASF à partir de l’objet ContentInfo dans la mémoire tampon du média créée à l’étape 4.

    La longueur des données dans la mémoire tampon du média est mise à jour et la nouvelle taille est retournée dans le paramètre *pcbHeader* .

6.  Écrire le contenu de la mémoire tampon du média au début du fichier. L’application peut utiliser le flux d’octets pour effectuer l’opération d’écriture. Pour obtenir un exemple de code, consultez [**IMFByteStream :: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

### <a name="example"></a>Exemple

L’exemple de code suivant montre comment créer un objet ContentInfo et générer une mémoire tampon de média pour stocker le nouvel objet d’en-tête. Pour obtenir un exemple complet qui utilise ce code, consultez [Didacticiel : copie de flux de fichiers ASF d’un fichier vers un autre](tutorial--copying-asf-streams-from-one-file-to-another.md).


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’un objet d’en-tête ASF pour un nouveau fichier](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



