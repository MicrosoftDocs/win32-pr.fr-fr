---
title: Inscription du fournisseur de services
description: Inscription du fournisseur de services
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Gestionnaire de périphériques de média, inscrire des fournisseurs de services
- Gestionnaire de périphériques, inscrire des fournisseurs de services
- Guide de programmation, inscrire des fournisseurs de services
- fournisseurs de services, inscrire des fournisseurs de services
- création de fournisseurs de services, inscription de fournisseurs de services
- inscription des fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919439"
---
# <a name="registering-the-service-provider"></a>Inscription du fournisseur de services

en plus d’être inscrit en tant qu’objet COM, un fournisseur de services doit être inscrit en tant que plug-in pour Windows Gestionnaire de périphériques de média. Pour s’inscrire, un fournisseur de services doit créer la clé de Registre suivante :

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

Dans cette clé, < le nom de votre *fournisseur de services* > est le nom de votre dll ; par exemple, l’exemple de fournisseur de services utilise MsHDSP. La clé ProgID doit avoir une valeur de chaîne qui correspond au CLSID de votre fournisseur de services. Par exemple, l’exemple de fournisseur de services a la valeur « MDServiceProviderHD. MDServiceProviderHD ».

L’exemple d’implémentation du fournisseur de services de DLLRegisterServer dans MDSP. cpp ajoute cette clé de registre lorsque vous inscrivez l’exemple de DLL du fournisseur de services.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’un fournisseur de services**](creating-a-service-provider.md)
</dt> </dl>

 

 




