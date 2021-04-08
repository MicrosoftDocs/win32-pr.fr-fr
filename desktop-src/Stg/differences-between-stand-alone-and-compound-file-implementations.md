---
title: Différences entre les implémentations de fichiers composés et autonomes
description: L’implémentation autonome des interfaces de jeu de propriétés et l’implémentation des fichiers composés diffèrent d’une certaine manière.
ms.assetid: 650d4759-a58a-47a4-922d-5757e356cf56
keywords:
- IPropertyStorage Strctd STG, implémentations
- IPropertyStorage Strctd STG, implémentations, différences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 988f8a9cfdaca0a131bedf98cd8ff10ae8b89525
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839830"
---
# <a name="differences-between-stand-alone-and-compound-file-implementations"></a>Différences entre les implémentations de fichiers composés et autonomes

L’implémentation autonome des interfaces de jeu de propriétés et l’implémentation des fichiers composés diffèrent d’une certaine manière. Dans l’implémentation de fichier composé de flux, stockage, stockage de jeu de propriétés et objets de stockage de propriétés, les différentes interfaces coordonnent les unes avec les autres, car elles partagent une implémentation commune. Dans l’implémentation autonome, les implémentations d’interface sont distinctes.

Par conséquent, l’implémentation de fichier composé gère les problèmes d’accès concurrentiel et synchronise l’objet de jeu de propriétés avec l’objet de stockage ou de flux. Avec l’implémentation autonome, le client est responsable de la gestion de l’accès concurrentiel et des problèmes de synchronisation entre l’objet de stockage ou de flux et le jeu de propriétés. Un client peut répondre à ces exigences en suivant deux règles simples. Tout d’abord, ne manipulez jamais un jeu de propriétés à l’aide de son flux ou de ses interfaces de stockage lorsqu’un objet de stockage de propriétés est ouvert dessus. Deuxièmement, appelez toujours **Commit** sur un objet de stockage de propriétés avant d’appeler **CopyTo**, **MoveElementTo** ou **Commit** sur un objet de stockage ancêtre. Plus précisément, les éléments suivants requièrent l’attention du client :

-   Dans l’implémentation de fichier composé, un mécanisme unique fournit une protection d’accès concurrentiel pour l’objet de stockage et ses objets de jeu de propriétés associés. Toutefois, dans l’implémentation autonome, l’implémentation de l’objet de stockage est distincte de l’implémentation du jeu de propriétés et chacune fournit ses propres mécanismes de concurrence. Ainsi, dans l’implémentation autonome, le client est responsable de la gestion de la protection d’accès concurrentiel entre les deux implémentations via un mécanisme d’exclusion mutuelle.
-   Dans l’implémentation de fichier composé, les modifications apportées aux jeux de propriétés sont mises en mémoire tampon dans un cache de jeu de propriétés. Ensuite, lorsque la méthode [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) est appelée sur l’objet de stockage, l’implémentation des fichiers composés vide automatiquement les modifications de l’ensemble de propriétés à partir de la mémoire tampon définie par la propriété avant la validation de l’objet de stockage. Ainsi, les modifications de l’ensemble de propriétés sont rendues visibles dans le cadre de la transaction en cours de validation.

    Dans l’implémentation autonome, le client doit vider explicitement la mémoire tampon de l’ensemble de propriétés en appelant [**IPropertyStorage :: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) avant d’appeler la méthode [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) sur le stockage. Le client peut également utiliser la nouvelle \_ valeur non mise en mémoire tampon PROPSETFLAG dans l’implémentation autonome pour écrire directement dans le jeu de propriétés au lieu de mettre en cache les modifications apportées à la mémoire tampon interne du jeu de propriétés. Si PROPSETFLAG \_ n’est pas mis en mémoire tampon, les responsabilités du client sont automatiquement respectées. L’implémentation de fichier composé ne prend pas en charge la \_ valeur non mise en mémoire tampon PROPSETFLAG. Pour plus d’informations, consultez [**constantes PROPSETFLAG**](propsetflag-constants.md).

-   Comme avec les stockages transactionnels, l’implémentation de fichiers composés met à jour le jeu de propriétés en vidant sa mémoire tampon interne avant d’exécuter un appel à [**IStorage :: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) ou [**IStorage :: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto). Ainsi, les modifications apportées au jeu de propriétés sont reflétées dans l’élément de stockage copié ou déplacé.

    Dans l’implémentation autonome, le client doit vider explicitement la mémoire tampon du jeu de propriétés en appelant [**IPropertyStorage :: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) avant d’appeler [**IStorage :: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) ou [**IStorage :: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto). Le client peut également utiliser la nouvelle \_ valeur non mise en mémoire tampon PROPSETFLAG pour écrire directement dans le jeu de propriétés au lieu de mettre en cache les modifications apportées à la mémoire tampon du jeu de propriétés. Pour plus d’informations, consultez [**constantes PROPSETFLAG**](propsetflag-constants.md).

 

 




