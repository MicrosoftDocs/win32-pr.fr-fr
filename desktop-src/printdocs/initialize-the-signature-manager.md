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
# <a name="initialize-the-signature-manager"></a>Initialiser le gestionnaire de signatures

Cette rubrique explique comment initialiser le gestionnaire de signature pour une utilisation avec un document XPS.

Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de signature numérique courantes](basic-digital-signature-programming-tasks.md).

Pour utiliser les fonctionnalités de Windows 7 de l’API de chiffrement, définissez les informations de chiffrement d’OID sur le symbole de **\_ \_ \_ \_ \_ champs supplémentaires** comme suit :


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



Ensuite, instanciez une interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), comme illustré dans l’exemple de code suivant.


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



L’interface instanciée par [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ne peut être utilisée que par un seul document XPS, qui doit être chargé en appelant [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) ou [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) avant d’appeler une autre méthode.

Une fois l’interface [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) instanciée et un document XPS chargé, le gestionnaire de signature est prêt à être utilisé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Next Steps**
</dt> <dt>

[Signer un document](sign-a-document.md)
</dt> <dt>

[Ajouter une demande de signature à un document XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Vérifier les signatures de document](verify-document-signatures.md)
</dt> <dt>

**Utilisé dans cette section**
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

**Pour plus d’informations**
</dt> <dt>

[Erreurs de l’API de signature numérique XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Erreurs de document XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
