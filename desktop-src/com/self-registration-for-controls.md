---
title: Inscription automatique pour les contrôles
description: Inscription automatique pour les contrôles
ms.assetid: 0fff07e5-10bb-4052-8eb1-021efcb66d6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdf2d71dcee1727031dd6ad9d55d88baf86a6b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008194"
---
# <a name="self-registration-for-controls"></a>Inscription automatique pour les contrôles

les contrôles ActiveX doivent prendre en charge l’inscription automatique en implémentant les fonctions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) et [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) . les contrôles de ActiveX doivent inscrire toutes les entrées de registre standard pour les objets et les serveurs automation incorporables.

les contrôles ActiveX doivent utiliser l’API des catégories de composants pour s’inscrire en tant que contrôle et enregistrer les catégories de composants qu’un hôte doit prendre en charge et toutes les catégories implémentées par le contrôle, consultez [catégories de composants](component-categories.md).

les contrôles ActiveX doivent également inscrire la clé de registre [ToolBoxBitmap32](toolboxbitmap32.md) , bien que cela ne soit pas obligatoire.

La catégorie de composant pouvant être insérée doit être inscrite uniquement si le contrôle peut être utilisé en tant qu’objet de document composé. il est important de noter qu’un objet de document composé doit prendre en charge certaines interfaces au-delà de la valeur de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) minimale requise pour un contrôle de ActiveX. bien qu’un contrôle de ActiveX puisse être qualifié d’objet de document composé, la documentation du contrôle doit indiquer clairement le comportement à attendre dans ces circonstances.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles](controls.md)
</dt> </dl>

 

 