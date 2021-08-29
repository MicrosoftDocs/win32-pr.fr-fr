---
title: Informations sur le manifeste du package d’application de requête (C++)
description: découvrez comment obtenir des informations à partir du manifeste de package d’application pour une application Windows à l’aide de l’API de packaging.
ms.assetid: A29986F9-C620-48CD-87F8-525DFA076AAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5407d19577fe917046e9664e9a946b3d9f4acc8c8a15cab1edfab2a934f0d93e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994179"
---
# <a name="query-app-package-manifest-info-c"></a>Informations sur le manifeste du package d’application de requête (C++)

découvrez comment obtenir des informations à partir du manifeste de package d’application pour une application Windows à l’aide de l' [API de packaging](interfaces.md).

### <a name="create-a-package-manifest-reader"></a>Créer un lecteur de manifeste du package

Pour créer un lecteur de manifeste de package, appelez [**IAppxFactory :: CreatePackageReader**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagereader) pour créer un lecteur de package. Le premier paramètre est un flux d’entrée pour le package (fichier. AppX). Le deuxième paramètre est un paramètre de sortie qui reçoit un pointeur vers un pointeur [**IAppxPackageReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagereader) . Ensuite, appelez [**IAppxPackageReader :: getmanifest**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagereader-getmanifest) pour accéder au lecteur du manifeste. Le paramètre est un paramètre de sortie qui reçoit un pointeur vers un pointeur [**IAppxManifestReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader) .


```C++
int wmain(
    _In_ int argc,
    _In_reads_(argc) wchar_t** argv)
{
    HRESULT hr = S_OK;
 
    if (argc != 2)
    {
        wprintf(L"Usage: DescribeAppx.exe inputFile\n");
        wprintf(L"       inputFile: Path to the app package to read\n");
        return 2;
    }

    // Specify the appropriate COM threading model
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (SUCCEEDED(hr))
    {
        IAppxPackageReader* packageReader = NULL;
        IAppxManifestReader* manifestReader = NULL;

        // Create a package reader using the file name given in command line
        hr = GetPackageReader(argv[1], &packageReader);

        // Get manifest reader for the package and read from the manifest
        if (SUCCEEDED(hr))
        {
            hr = packageReader->GetManifest(&manifestReader);
        }
        if (SUCCEEDED(hr))
        {
            hr = ReadManifest(manifestReader);
        }
    }
}

//
// Creates an app package reader.
//
// Parameters:
//   inputFileName 
//     Fully qualified name of the app package (.appx file) to be opened.
//   reader 
//     On success, receives the created instance of IAppxPackageReader.
//
HRESULT GetPackageReader(
    _In_ LPCWSTR inputFileName,
    _Outptr_ IAppxPackageReader** reader)
{
    HRESULT hr = S_OK;
    IAppxFactory* appxFactory = NULL;
    IStream* inputStream = NULL;

    // Create a new factory
    hr = CoCreateInstance(
            __uuidof(AppxFactory),
            NULL,
            CLSCTX_INPROC_SERVER,
            __uuidof(IAppxFactory),
            (LPVOID*)(&appxFactory));

    // Create a stream over the input app package
    if (SUCCEEDED(hr))
    {
        hr = SHCreateStreamOnFileEx(
                inputFileName,
                STGM_READ | STGM_SHARE_EXCLUSIVE,
                0, // default file attributes
                FALSE, // do not create new file
                NULL, // no template
                &inputStream);
    }

    // Create a new package reader using the factory.  For 
    // simplicity, we don't verify the digital signature of the package.
    if (SUCCEEDED(hr))
    {
        hr = appxFactory->CreatePackageReader(
                inputStream,
                reader);
    }

    // Clean up allocated resources
    if (inputStream != NULL)
    {
        inputStream->Release();
        inputStream = NULL;
    }
    if (appxFactory != NULL)
    {
        appxFactory->Release();
        appxFactory = NULL;
    }
    return hr;
}
```



### <a name="read-package-identity-info"></a>Lire les informations d’identité du package

L’identification du package est spécifiée à l’aide de l’élément [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) dans le manifeste. Utilisez [**IAppxManifestReader :: GetPackageId**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getpackageid) pour obtenir un [**IAppxManifestPackageId**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestpackageid) afin de lire les informations d’identité du package, comme illustré ici.

Ce code utilise [**IAppxManifestPackageId :: GetPackageFullName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getpackagefullname) pour obtenir le nom complet du package, [**IAppxManifestPackageId :: GetName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getname) pour obtenir le nom du package, et [**IAppxManifestPackageId :: GetVersion**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getversion) pour obtenir la version du package.


```C++
//
// Reads a subset of the manifest Identity element.
//
//
HRESULT ReadManifestPackageId(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestPackageId* packageId = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetPackageId(&packageId);
    if (SUCCEEDED(hr))
    {
        LPWSTR packageFullName = NULL;
        LPWSTR packageName = NULL;
        UINT64 packageVersion = 0;

        hr = packageId->GetPackageFullName(&packageFullName);

        if (SUCCEEDED(hr))
        {
            hr = packageId->GetName(&packageName);
        }
        if (SUCCEEDED(hr))
        {
            hr = packageId->GetVersion(&packageVersion);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package full name: %s\n", packageFullName);
            wprintf(L"Package name: %s\n", packageName);
            wprintf(L"Package version: ");

            // Convert version number from 64-bit integer to dot-quad form
            for (int bitPosition = 0x30; bitPosition >= 0; bitPosition -= 0x10)
            {
                UINT64 versionWord = (packageVersion >> bitPosition) & 0xFFFF;
                wprintf(L"%llu.", versionWord);
            }
            wprintf(L"\n");
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(packageFullName);
        CoTaskMemFree(packageName);
    }

    // Clean up allocated resources
    if (packageId != NULL)
    {
        packageId->Release();
        packageId = NULL;
    }
     
    return hr;
}
```



### <a name="read-metadata-that-describes-the-package-to-users"></a>Lire les métadonnées qui décrivent le package aux utilisateurs

Les propriétés sont spécifiées à l’aide de l’élément [**Properties**](/uwp/schemas/appxpackage/appxmanifestschema/element-properties) dans le manifeste. Utilisez [**IAppxManifestReader :: GetProperties**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getproperties) pour obtenir un [**IAppxManifestProperties**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestproperties) pour lire ce nœud, comme illustré ici.

Ce code utilise [**IAppxManifestProperties :: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestproperties-getstringvalue) pour obtenir le nom complet du package et la description du package.


```C++
//
// Reads a subset of the manifest Properties element.
//
//
HRESULT ReadManifestProperties(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestProperties* properties = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetProperties(&properties);
    if (SUCCEEDED(hr))
    {
        LPWSTR displayName = NULL;
        LPWSTR description = NULL;

        hr = properties->GetStringValue(L"DisplayName", &displayName);

        if (SUCCEEDED(hr))
        {
            hr = properties->GetStringValue(L"Description", &description);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package display name: %s\n", displayName);
            wprintf(L"Package description:  %s\n", description);
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(displayName);
        CoTaskMemFree(description);
    }
    // Clean up allocated resources
    if (properties != NULL)
    {
        properties->Release();
        properties = NULL;
    }

    return hr;
}
```



### <a name="read-metadata-about-the-apps-included-in-the-package"></a>Lire les métadonnées relatives aux applications incluses dans le package

Les applications sont spécifiées à l’aide de l’élément [**applications**](/uwp/schemas/appxpackage/appxmanifestschema/element-applications) dans le manifeste. Utilisez [**IAppxManifestReader :: GetApplications**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getapplications) pour obtenir un [**IAppxManifestApplicationsEnumerator**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator) pour lire ce nœud. Utilisez [**IAppxManifestApplicationsEnumerator :: GetCurrent**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-getcurrent) et [**IAppxManifestApplicationsEnumerator :: MoveNext**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext) pour obtenir un [**IAppxManifestApplication**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplication) pour chaque application dans le package.

Ce code utilise [**IAppxManifestApplication :: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplication-getstringvalue) pour obtenir le nom complet de chaque application.


```C++
//
// Reads a subset of the manifest Applications element.
//
//
HRESULT ReadManifestApplications(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;
    BOOL hasCurrent = FALSE;
    UINT32 applicationsCount = 0;

    IAppxManifestApplicationsEnumerator* applications = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetApplications(&applications);
    if (SUCCEEDED(hr))
    {
        hr = applications->GetHasCurrent(&hasCurrent);

        while (SUCCEEDED(hr) && hasCurrent)
        {
            IAppxManifestApplication* application = NULL;
            LPWSTR applicationName = NULL;

            hr = applications->GetCurrent(&application);
            if (SUCCEEDED(hr))
            {
                application->GetStringValue(L"DisplayName", &applicationName);
            }
            if (SUCCEEDED(hr))
            {
                applicationsCount++;
                wprintf(L"App #%u: %s\n", applicationsCount, applicationName);
            }

            if (SUCCEEDED(hr))
            {
                hr = applications->MoveNext(&hasCurrent);
            }
            if (application != NULL)
            {
                application->Release();
                application = NULL;
            }
            CoTaskMemFree(applicationName);
        }

        wprintf(L"Count of apps in the package: %u\n", applicationsCount);
    }

    // Clean up allocated resources
    if (applications != NULL)
    {
        applications->Release();
        applications = NULL;
    }

    return hr;
}
```



### <a name="clean-up-the-package-manifest-reader"></a>Nettoyer le lecteur du manifeste du package

Avant de retourner à partir de la `wmain` fonction, appelez la méthode [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) pour nettoyer le lecteur du manifeste du package et appelez la fonction [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) .


```C++
// Clean up allocated resources
if (manifestReader != NULL)
{
    manifestReader->Release();
    manifestReader = NULL;
}
if (packageReader != NULL)
{
    packageReader->Release();
    packageReader = NULL;
}

CoUninitialize();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Exemples**
</dt> <dt>

[Exemple de package d’application de requête et de manifeste d’application](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx)
</dt> <dt>

**Référence**
</dt> <dt>

[**IAppxManifestReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader)
</dt> </dl>

 

 