---
title: Inscription automatique pour les contrôles
description: Inscription automatique pour les contrôles
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106511715"
---
# <a name="self-registration-for-controls"></a>Inscription automatique pour les contrôles

Les contrôles ActiveX doivent prendre en charge l’inscription automatique en implémentant les fonctions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) . Les contrôles ActiveX doivent inscrire toutes les entrées de Registre standard pour les objets et les serveurs Automation incorporables.

Les contrôles ActiveX doivent utiliser l’API des catégories de composants pour s’inscrire en tant que contrôle et enregistrer les catégories de composants qu’un hôte doit prendre en charge et toutes les catégories implémentées par le contrôle, consultez [catégories de composants](component-categories.md).

Les contrôles ActiveX doivent également inscrire la clé de Registre [ToolboxBitmap32](toolboxbitmap32.md) , bien que cela ne soit pas obligatoire.

La catégorie de composant pouvant être insérée doit être inscrite uniquement si le contrôle peut être utilisé en tant qu’objet de document composé. Il est important de noter qu’un objet de document composé doit prendre en charge certaines interfaces au-delà de la valeur de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) minimale requise pour un contrôle ActiveX. Bien qu’un contrôle ActiveX puisse être qualifié d’objet de document composé, la documentation du contrôle doit indiquer clairement le comportement à attendre dans ces circonstances.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles](controls.md)
</dt> </dl>

 

 