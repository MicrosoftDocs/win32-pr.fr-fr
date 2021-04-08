---
title: Utilisation d’attributs ACF dans un fichier IDL
description: Vous pouvez utiliser l' \_ option du compilateur MIDL de configuration/App pour spécifier des attributs de handle de liaison dans le fichier IDL plutôt que dans un fichier ACF distinct.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- ACF MIDL, attributs, utilisation de ACF dans IDL
- MIDL MIDL, utilisation de ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712dde95201bc2c729ac126b35e04919fd196cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672742"
---
# <a name="using-acf-attributes-in-an-idl-file"></a><span data-ttu-id="01330-105">Utilisation d’attributs ACF dans un fichier IDL</span><span class="sxs-lookup"><span data-stu-id="01330-105">Using ACF Attributes in an IDL File</span></span>

<span data-ttu-id="01330-106">Vous pouvez utiliser l’option du compilateur MIDL/[**\_ configuration**](-app-config.md) de l’application pour spécifier des attributs de handle de liaison dans le fichier IDL plutôt que dans un fichier ACF distinct.</span><span class="sxs-lookup"><span data-stu-id="01330-106">You can use the /[**app\_config**](-app-config.md) MIDL compiler option to specify binding handle attributes in the IDL file rather than in a separate ACF file.</span></span> <span data-ttu-id="01330-107">Plus précisément, vous pouvez appliquer les attributs handle [**automatique \_**](auto-handle.md), descripteur [**implicite \_**](implicit-handle.md)et [**\_ handle explicite**](explicit-handle.md) à l’en-tête d’une interface RPC dans un fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="01330-107">Specifically, you can apply the [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), and [**explicit\_handle**](explicit-handle.md) attributes to the header of an RPC interface in an IDL file.</span></span> <span data-ttu-id="01330-108">Envisagez d’utiliser cette option si votre application RPC ne nécessite pas d’autres attributs ACF et si vous n’avez pas besoin d’une compatibilité OSF-DCE stricte.</span><span class="sxs-lookup"><span data-stu-id="01330-108">Consider using this option if your RPC application does not require other ACF attributes, and if you do not require strict OSF-DCE compatibility.</span></span>

 

 




