---
title: En-tête ACF
description: L’en-tête ACF contient des attributs spécifiques à la plateforme qui s’appliquent à l’ensemble de l’interface. Les attributs appliqués aux types et aux fonctions individuels dans le corps ACF remplacent les attributs dans l’en-tête ACF. Aucun attribut n’est requis dans l’en-tête ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdfeced843337143fd441d816e3b575be2e7ebc7d93000094f8dcd3737a00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924609"
---
# <a name="the-acf-header"></a>En-tête ACF

L’en-tête ACF contient des attributs spécifiques à la plateforme qui s’appliquent à l’ensemble de l’interface. Les attributs appliqués aux types et aux fonctions individuels dans le corps ACF remplacent les attributs dans l’en-tête ACF. Aucun attribut n’est requis dans l’en-tête ACF.

L’en-tête ACF peut inclure l’un des attributs suivants : **\[** [**\_ handle automatique**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**\_ handle implicite**](/windows/desktop/Midl/implicit-handle) **\]** ou [**\_ handle explicite**](/windows/desktop/Midl/explicit-handle) **\]** . Si le **\[ \_ handle \] automatique** ou le **\[ \_ \] handle implicite** est utilisé, il spécifie le type de handle de liaison qui sera utilisé pour la liaison lorsqu’une fonction distante n’a pas de paramètre de handle de liaison explicite. Lorsque le ACF n’est pas présent ou qu’il ne spécifie pas un handle de liaison automatique, implicite ou explicite, MIDL utilise le **\[ \_ handle \] automatique** pour la liaison implicite.

Le **\[** [**code**](/windows/desktop/Midl/code) **\]** ou le **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** peut apparaître dans l’en-tête de l’interface, mais celui que vous choisissez ne peut apparaître qu’une seule fois. Quand aucun attribut n’est présent, le compilateur utilise le **\[ code \]** comme valeur par défaut.

Pour plus d’informations, consultez la rubrique [attributs ACF](/windows/desktop/Midl/acf-attributes).

 

 