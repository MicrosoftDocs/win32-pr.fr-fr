---
description: Cette rubrique explique comment initialiser le gestionnaire de signature pour une utilisation avec un document XPS.
ms.assetid: 4c4c6e8f-4ee0-4089-a283-1082baee5054
title: Initialiser le gestionnaire de signatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2796838a9cd041859f0eb47bf4aeafb2a8d5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536644"
---
# <a name="initialize-the-signature-manager"></a><span data-ttu-id="7c797-103">Initialiser le gestionnaire de signatures</span><span class="sxs-lookup"><span data-stu-id="7c797-103">Initialize the Signature Manager</span></span>

<span data-ttu-id="7c797-104">Cette rubrique explique comment initialiser le gestionnaire de signature pour une utilisation avec un document XPS.</span><span class="sxs-lookup"><span data-stu-id="7c797-104">This topic describes how to initialize the signature manager for use with an XPS document.</span></span>

<span data-ttu-id="7c797-105">Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de signature numérique courantes](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="7c797-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="7c797-106">Pour utiliser les fonctionnalités de Windows 7 de l’API de chiffrement, définissez les informations de chiffrement d’OID sur le symbole de **\_ \_ \_ \_ \_ champs supplémentaires** comme suit :</span><span class="sxs-lookup"><span data-stu-id="7c797-106">To use the Windows 7 features of the Crypto API, define the **CRYPT\_OID\_INFO\_HAS\_EXTRA\_FIELDS** symbol as follows:</span></span>


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



<span data-ttu-id="7c797-107">Ensuite, instanciez une interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7c797-107">Next, instantiate an [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), as shown in the following code example.</span></span>


```C++
IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast<LPVOID*>(&newInterface));

// make sure that you got a pointer 
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface->LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them 
    newInterface->Release();
}    
```



<span data-ttu-id="7c797-108">L’interface instanciée par [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ne peut être utilisée que par un seul document XPS, qui doit être chargé en appelant [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) ou [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) avant d’appeler une autre méthode.</span><span class="sxs-lookup"><span data-stu-id="7c797-108">The interface instantiated by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) can be used by only one XPS document, which must be loaded by calling [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) or [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) before calling any other method.</span></span>

<span data-ttu-id="7c797-109">Une fois l’interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) instanciée et un document XPS chargé, le gestionnaire de signature est prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="7c797-109">After the [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface has been instantiated and an XPS document has been loaded, the signature manager is ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c797-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c797-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7c797-111">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="7c797-111">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="7c797-112">Signer un document</span><span class="sxs-lookup"><span data-stu-id="7c797-112">Sign a Document</span></span>](sign-a-document.md)
</dt> <dt>

[<span data-ttu-id="7c797-113">Ajouter une demande de signature à un document XPS</span><span class="sxs-lookup"><span data-stu-id="7c797-113">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="7c797-114">Vérifier les signatures de document</span><span class="sxs-lookup"><span data-stu-id="7c797-114">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="7c797-115">**Utilisé dans cette section**</span><span class="sxs-lookup"><span data-stu-id="7c797-115">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="7c797-116">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="7c797-116">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="7c797-117">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="7c797-117">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

<span data-ttu-id="7c797-118">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="7c797-118">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="7c797-119">Erreurs de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="7c797-119">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="7c797-120">Erreurs de document XPS</span><span class="sxs-lookup"><span data-stu-id="7c797-120">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="7c797-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="7c797-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
