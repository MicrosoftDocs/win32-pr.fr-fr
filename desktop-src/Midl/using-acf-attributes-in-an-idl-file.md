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
# <a name="using-acf-attributes-in-an-idl-file"></a>Utilisation d’attributs ACF dans un fichier IDL

Vous pouvez utiliser l’option du compilateur MIDL/[**\_ configuration**](-app-config.md) de l’application pour spécifier des attributs de handle de liaison dans le fichier IDL plutôt que dans un fichier ACF distinct. Plus précisément, vous pouvez appliquer les attributs handle [**automatique \_**](auto-handle.md), descripteur [**implicite \_**](implicit-handle.md)et [**\_ handle explicite**](explicit-handle.md) à l’en-tête d’une interface RPC dans un fichier IDL. Envisagez d’utiliser cette option si votre application RPC ne nécessite pas d’autres attributs ACF et si vous n’avez pas besoin d’une compatibilité OSF-DCE stricte.

 

 




