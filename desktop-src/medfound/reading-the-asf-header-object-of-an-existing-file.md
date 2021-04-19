---
description: Lecture de l’objet d’en-tête ASF d’un fichier existant
ms.assetid: 0e37f0d3-a37b-4f36-a133-7b1922e9944b
title: Lecture de l’objet d’en-tête ASF d’un fichier existant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b231cb0b9af6b24f84efaa6403a4774e66bbb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524943"
---
# <a name="reading-the-asf-header-object-of-an-existing-file"></a><span data-ttu-id="c5797-103">Lecture de l’objet d’en-tête ASF d’un fichier existant</span><span class="sxs-lookup"><span data-stu-id="c5797-103">Reading the ASF Header Object of an Existing File</span></span>

<span data-ttu-id="c5797-104">L’objet ASF ContentInfo stocke des informations qui représentent les objets d’en-tête ASF d’un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="c5797-104">The ASF ContentInfo object stores information that represents the ASF Header Objects of a media file.</span></span> <span data-ttu-id="c5797-105">Un objet ContentInfo rempli est requis pour lire et analyser un fichier ASF existant.</span><span class="sxs-lookup"><span data-stu-id="c5797-105">A populated ContentInfo object is required in order to read and parse an existing ASF file.</span></span>

<span data-ttu-id="c5797-106">Après avoir créé l’objet ContentInfo en appelant la fonction [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) , l’application doit l’initialiser avec les informations d’en-tête du fichier ASF à lire.</span><span class="sxs-lookup"><span data-stu-id="c5797-106">After creating the ContentInfo object by calling the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function, the application must initialize it with header information from the ASF file that is to be read.</span></span> <span data-ttu-id="c5797-107">Pour remplir l’objet, appelez [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span><span class="sxs-lookup"><span data-stu-id="c5797-107">To populate the object, call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader).</span></span>

<span data-ttu-id="c5797-108">**ParseHeader** requiert une mémoire tampon de média qui contient l’objet d’en-tête du fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="c5797-108">**ParseHeader** requires a media buffer that contains the Header Object of the ASF file.</span></span> <span data-ttu-id="c5797-109">L’une des options consiste à remplir un tampon de média avec l’objet d’en-tête pour créer un flux d’octets pour le fichier, puis à lire les 30 premiers octets de données à partir du flux d’octets dans une mémoire tampon de média.</span><span class="sxs-lookup"><span data-stu-id="c5797-109">One option is to fill a media buffer with the Header Object to create a byte stream for the file and then read the first 30 bytes of data from the byte stream into a media buffer.</span></span> <span data-ttu-id="c5797-110">Vous pouvez ensuite récupérer la taille en passant les 24 premiers octets de l’objet d’en-tête à la méthode [**IMFASFContentInfo :: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="c5797-110">You can then get the size by passing the first 24 bytes of the Header Object to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="c5797-111">Après avoir obtenu la taille, vous pouvez lire l’objet d’en-tête entier dans une mémoire tampon de média et la passer à **ParseHeader**.</span><span class="sxs-lookup"><span data-stu-id="c5797-111">After getting the size, you can read the entire Header Object in a media buffer and pass it to **ParseHeader**.</span></span> <span data-ttu-id="c5797-112">La méthode commence l’analyse au décalage à partir du début de la mémoire tampon du média spécifiée dans le paramètre *cbOffsetWithinHeader* .</span><span class="sxs-lookup"><span data-stu-id="c5797-112">The method starts parsing at the offset from the start of the media buffer specified in the *cbOffsetWithinHeader* parameter.</span></span>

<span data-ttu-id="c5797-113">L’exemple de code suivant crée et initialise un objet ContentInfo pour la lecture d’un fichier ASF existant contenu dans un flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="c5797-113">The following example code creates and initializes a ContentInfo object for reading an existing ASF file contained in a byte stream.</span></span> <span data-ttu-id="c5797-114">Tout d’abord, nous définissons une fonction d’assistance qui lit les données à partir d’un flux d’octets et alloue une mémoire tampon de média pour contenir les données :</span><span class="sxs-lookup"><span data-stu-id="c5797-114">First, we define a helper function that reads data from a byte stream and allocates a media buffer to hold the data:</span></span>


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



<span data-ttu-id="c5797-115">L’exemple suivant lit l’objet d’en-tête ASF à partir d’un flux d’octets et remplit un objet ASF ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="c5797-115">The next example reads the ASF Header Object from a byte stream and populates an ASF ContentInfo object.</span></span>


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



> [!Note]  
> <span data-ttu-id="c5797-116">Ces exemples utilisent la fonction [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface.</span><span class="sxs-lookup"><span data-stu-id="c5797-116">These examples use the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c5797-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5797-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5797-118">Objet ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="c5797-118">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
</dt> <dt>

[<span data-ttu-id="c5797-119">Objet d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="c5797-119">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="c5797-120">Prise en charge ASF dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5797-120">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="c5797-121">Obtention d’informations à partir d’objets d’en-tête ASF</span><span class="sxs-lookup"><span data-stu-id="c5797-121">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
</dt> </dl>

 

 



