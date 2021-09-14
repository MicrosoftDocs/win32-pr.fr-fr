---
description: à partir de Windows 8, Microsoft a commencé à distribuer les fournisseurs qui vous permettent de partager en toute sécurité des secrets et des messages chiffrés sur les ordinateurs.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Fournisseurs de protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013652"
---
# <a name="protection-providers"></a>Fournisseurs de protection

à partir de Windows 8, Microsoft a commencé à distribuer les fournisseurs qui vous permettent de partager en toute sécurité des secrets et des messages chiffrés sur les ordinateurs. Il existe actuellement deux fournisseurs de protection de clé. Le fournisseur de protection de clé Microsoft vous permet de protéger le contenu d’un groupe dans une forêt Active Directory. Le fournisseur de protection de clé client Microsoft vous permet de protéger le contenu d’un ensemble d’informations d’identification Web.

Le protecteur approprié à utiliser est automatiquement choisi lorsque la fonction [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) analyse la chaîne de règle du descripteur de protection que vous fournissez en tant qu’entrée. Le fournisseur de protection de clé Microsoft est choisi pour les chaînes de règle qui commencent par SID, SDDL et LOCAL. Le fournisseur de protection de clé client Microsoft analyse les chaînes de règles qui commencent par webinformation. Pour plus d’informations sur les chaînes de règle, consultez [descripteurs de protection](protection-descriptors.md).

> [!Note]  
> Les fournisseurs personnalisés ne sont pas autorisés actuellement. [DPAPI CNG](cng-dpapi.md)

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DPAPI CNG](cng-dpapi.md)
</dt> <dt>

[**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[Descripteurs de protection](protection-descriptors.md)
</dt> </dl>

 

 



