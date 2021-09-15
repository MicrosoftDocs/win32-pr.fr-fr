---
description: Compatibilité DEP/NX
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilité DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b46c9143ee96b8599c10d4c70276d36e20a08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531528"
---
# <a name="depnx-compatibility"></a>Compatibilité DEP/NX

par défaut, dans Windows Internet Explorer 7, DEP/NX est désactivé pour des raisons de compatibilité. plusieurs modules complémentaires populaires ne sont pas compatibles avec dep/nx et échouent quand Windows Internet Explorer les charge avec dep/nx activé.

En règle générale, ces modules complémentaires sont générés à l’aide d’une version antérieure de l’infrastructure ATL. ATL 7,1 et les versions antérieures ne sont pas conçus avec la fonctionnalité de sécurité DEP. heureusement, les nouvelles versions des service packs Microsoft Windows disposent de nouvelles api dep/nx qui vous permettent d’utiliser dep/nx et de conserver la compatibilité avec les anciennes versions d’ATL. Ces nouvelles API permettent à Internet Explorer de s’abonner à DEP/NX sans entraîner l’échec des modules complémentaires générés à l’aide de versions antérieures d’ATL.

Lorsqu’un module complémentaire n’est pas compatible avec DEP/NX et qu’il n’utilise pas d’ATL obsolète, vous pouvez utiliser une option stratégie de groupe pour refuser DEP/NX pour Internet Explorer jusqu’à ce qu’une version mise à jour du contrôle endommagé soit déployée. Les administrateurs locaux peuvent contrôler DEP/NX en exécutant Internet Explorer en tant qu’administrateur et en désactivant l’option **activer la protection** de la mémoire dans le volet **avancé** des **Options Internet**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
