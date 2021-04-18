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
# <a name="generating-a-new-asf-header-object"></a><span data-ttu-id="f881e-103">Génération d’un nouvel objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="f881e-103">Generating a New ASF Header Object</span></span>

<span data-ttu-id="f881e-104">Pour convertir les informations contenues dans l’objet ContentInfo en un format d’objet d’en-tête ASF binaire, l’application doit appeler [**IMFASFContentInfo :: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="f881e-104">To convert the information contained in the ContentInfo object to a binary ASF Header Object format, the application must call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="f881e-105">Cet appel doit être effectué après la génération des paquets de données et l’objet ContentInfo contient des informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f881e-105">This call must be made after the data packets are generated and the ContentInfo object contains updated information.</span></span> <span data-ttu-id="f881e-106">**GenerateHeader** retourne un pointeur vers une mémoire tampon de média qui contient les informations d’en-tête dans le format valide.</span><span class="sxs-lookup"><span data-stu-id="f881e-106">**GenerateHeader** returns a pointer to a media buffer that contains the header information in the valid format.</span></span> <span data-ttu-id="f881e-107">L’application peut ensuite écrire les données, pointées par la mémoire tampon du média, au début d’un nouveau fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="f881e-107">The application can then write the data, pointed to by the media buffer, at the beginning of a new ASF file.</span></span>

## <a name="to-write-a-new-header-object-by-using-the-contentinfo-object"></a><span data-ttu-id="f881e-108">Pour écrire un nouvel objet d’en-tête à l’aide de l’objet ContentInfo</span><span class="sxs-lookup"><span data-stu-id="f881e-108">To write a new Header Object by using the ContentInfo object</span></span>

1.  <span data-ttu-id="f881e-109">Appelez [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) pour créer un objet ContentInfo vide.</span><span class="sxs-lookup"><span data-stu-id="f881e-109">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="f881e-110">Appelez [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) pour fournir l’objet de profil à l’objet ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="f881e-110">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to supply the profile object to the ContentInfo object.</span></span> <span data-ttu-id="f881e-111">Pour plus d’informations sur la création de profils, consultez [création d’un profil ASF](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="f881e-111">For information about creating profiles, see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
3.  <span data-ttu-id="f881e-112">Appelez [**IMFASFContentInfo :: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) et transmettez **null** dans le paramètre *pIHeader* et recevez la taille de l’objet ContentInfo rempli dans le paramètre *pcbHeader* .</span><span class="sxs-lookup"><span data-stu-id="f881e-112">Call [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader) and pass **NULL** in the *pIHeader* parameter and receive the size of the populated ContentInfo object in the *pcbHeader* parameter.</span></span> <span data-ttu-id="f881e-113">L’application peut utiliser cette valeur pour allouer de la mémoire ou la mémoire tampon du média qui contiendra l’objet d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f881e-113">The application can use this value to allocate memory or the media buffer that will contain the Header Object.</span></span>

    <span data-ttu-id="f881e-114">La taille d’en-tête reçue comprend la taille de remplissage, qui est ajustée en fonction de la taille réelle des objets d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f881e-114">The header size received includes the padding size, which is adjusted depending on the actual size of the header objects.</span></span> <span data-ttu-id="f881e-115">La taille maximale des objets d’en-tête est de 10 Mo.</span><span class="sxs-lookup"><span data-stu-id="f881e-115">The maximum size of the header objects is 10 MB.</span></span> <span data-ttu-id="f881e-116">Si la taille dépasse cette valeur, **GenerateHeader** échoue avec l' \_ erreur MF E \_ ASF \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="f881e-116">If the size exceeds this value, **GenerateHeader** fails with the MF\_E\_ASF\_INVALIDDATA error.</span></span>

4.  <span data-ttu-id="f881e-117">Appelez [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) pour créer une mémoire tampon de média de la taille reçue à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="f881e-117">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer of the received size in step 3.</span></span>
5.  <span data-ttu-id="f881e-118">Appelez à nouveau **GenerateHeader** pour générer le nouvel objet d’en-tête ASF à partir de l’objet ContentInfo dans la mémoire tampon du média créée à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="f881e-118">Call **GenerateHeader** again to generate the new ASF Header Object from the ContentInfo object in the media buffer created in step 4.</span></span>

    <span data-ttu-id="f881e-119">La longueur des données dans la mémoire tampon du média est mise à jour et la nouvelle taille est retournée dans le paramètre *pcbHeader* .</span><span class="sxs-lookup"><span data-stu-id="f881e-119">The length of the data in the media buffer is updated and the new size is returned in the *pcbHeader* parameter.</span></span>

6.  <span data-ttu-id="f881e-120">Écrire le contenu de la mémoire tampon du média au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="f881e-120">Write the contents of the media buffer at the beginning of the file.</span></span> <span data-ttu-id="f881e-121">L’application peut utiliser le flux d’octets pour effectuer l’opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="f881e-121">The application can use the byte stream to perform the writing operation.</span></span> <span data-ttu-id="f881e-122">Pour obtenir un exemple de code, consultez [**IMFByteStream :: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="f881e-122">For example code, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>

### <a name="example"></a><span data-ttu-id="f881e-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="f881e-123">Example</span></span>

<span data-ttu-id="f881e-124">L’exemple de code suivant montre comment créer un objet ContentInfo et générer une mémoire tampon de média pour stocker le nouvel objet d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f881e-124">The following example code shows how to create a ContentInfo object and generate a media buffer to store the new Header Object.</span></span> <span data-ttu-id="f881e-125">Pour obtenir un exemple complet qui utilise ce code, consultez [Didacticiel : copie de flux de fichiers ASF d’un fichier vers un autre](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="f881e-125">For a complete example that uses this code, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f881e-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f881e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f881e-127">Écriture d’un objet d’en-tête ASF pour un nouveau fichier</span><span class="sxs-lookup"><span data-stu-id="f881e-127">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



