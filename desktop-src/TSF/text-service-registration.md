---
title: Inscription du service de texte
description: En plus des entrées de Registre du serveur in-proc COM standard, un service de texte doit s’inscrire auprès de Text Services Framework (TSF) pour pouvoir être utilisé avec une application.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- Text Services Framework (TSF), inscription
- TSF (Text Services Framework), inscription
- services de texte, inscription
- Text Services Framework (TSF), profils de langue
- TSF (Text Services Framework), profils de langue
- services de texte, profils de langue
- Text Services Framework (TSF), catégories
- TSF (Text Services Framework), catégories
- services de texte, catégories
- inscription des services de texte
- inscription des profils de langue
- inscription des catégories
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463399"
---
# <a name="text-service-registration"></a>Inscription du service de texte

En plus des entrées de Registre du serveur in-proc COM standard, un service de texte doit s’inscrire auprès de Text Services Framework (TSF) pour pouvoir être utilisé avec une application. TSF fournit l’interface [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) et [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) pour simplifier le processus d’inscription.

Les fournisseurs de services de texte doivent également fournir des signatures numériques avec leurs exécutables binaires. Consultez [Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).

## <a name="registering-the-text-service"></a>Inscription du service de texte

Un service de texte s’inscrit auprès de TSF en appelant [ITfInputProcessorProfiles :: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) avec l’identificateur de classe du service de texte. Une instance de l’interface **ITfInputProcessorProfiles** est obtenue en appelant **COCREATEINSTANCE** avec le CLSID \_ tf \_ InputProcessorProfiles.

L’exemple suivant montre comment créer un objet **ITfInputProcessorProfiles** et inscrire le service de texte.


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[ITfInputProcessorProfiles :: Unregister](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a>Inscription des profils de langue

Un service de texte est disponible uniquement lorsqu’une application a le focus et que la langue appropriée est sélectionnée dans la barre de langue. Pour faciliter cette opération, TSF requiert qu’un service de texte s’inscrit lui-même pour tous les langages qu’il prend en charge. Le service de texte inscrit ses profils de langage en appelant [ITfInputProcessorProfiles :: AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) avec l’identificateur de classe de service de texte, cet identificateur de langue du profil et un **GUID** défini par le service de texte qui identifie le profil de langue.

Vous pouvez supprimer un profil de langue en appelant [ITfInputProcessorProfiles :: RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile). **ITfInputProcessorProfiles :: Unregister** supprime tous les profils de langue pour le service de texte ; Lorsqu’un service de texte est désinstallé, il est nécessaire de supprimer les profils de langue individuels.

## <a name="registering-categories"></a>Inscription des catégories

Un service de texte doit également inscrire la catégorie à laquelle s’applique le service de texte. Par exemple, si le service de texte fournit des informations sur les attributs d’affichage, il doit s’inscrire en tant que fournisseur d’attributs d’affichage en appelant [ITfCategoryMgr :: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) avec l’identificateur de classe du service de texte pour le premier paramètre, Guid \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER pour le deuxième paramètre et l’identificateur de classe du service de texte pour le troisième paramètre. Les catégories possibles sont répertoriées sous [valeurs des catégories prédéfinies](predefined-category-values.md).

Supprimez les catégories précédemment inscrites en appelant [ITfCategoryMgr :: UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory). ITfInputProcessorProfiles :: unregister Supprime toutes les catégories pour le service de texte ; Lorsqu’un service de texte est désinstallé, il doit supprimer les différentes catégories.

 

 