---
title: Utilisation d’attributs ACF dans un fichier IDL
description: Vous pouvez utiliser l' \_ option du compilateur MIDL de configuration/App pour spécifier des attributs de handle de liaison dans le fichier IDL plutôt que dans un fichier ACF distinct.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- ACF MIDL, attributs, utilisation de ACF dans IDL
- MIDL MIDL, utilisation de ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda925a3b3242072f297c8828427ae4f7a488d1f3b002e05ace6bec45a46d2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105519"
---
# <a name="using-acf-attributes-in-an-idl-file"></a>Utilisation d’attributs ACF dans un fichier IDL

Vous pouvez utiliser l’option du compilateur MIDL/[**\_ configuration**](-app-config.md) de l’application pour spécifier des attributs de handle de liaison dans le fichier IDL plutôt que dans un fichier ACF distinct. Plus précisément, vous pouvez appliquer les attributs handle [**automatique \_**](auto-handle.md), descripteur [**implicite \_**](implicit-handle.md)et [**\_ handle explicite**](explicit-handle.md) à l’en-tête d’une interface RPC dans un fichier IDL. Envisagez d’utiliser cette option si votre application RPC ne nécessite pas d’autres attributs ACF et si vous n’avez pas besoin d’une compatibilité OSF-DCE stricte.

 

 




