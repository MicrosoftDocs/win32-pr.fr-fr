---
description: Format MOF (MOF) est le langage utilisé pour décrire les classes Common Information Model (CIM).
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: Managed Object Format (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ac36bd89979d6cf0de0a4d574a47a6ce7060f90e5577402eba77aa2de42bbedb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131175"
---
# <a name="managed-object-format-mof"></a>Managed Object Format (MOF)

Format MOF (MOF) est le langage utilisé pour décrire les classes [*Common Information Model (CIM)*](gloss-c.md) .

La méthode recommandée pour les fournisseurs WMI pour implémenter les nouvelles classes WMI est dans les fichiers MOF qui sont compilés à l’aide de [**Mofcomp.exe**](mofcomp.md) dans le [*référentiel WMI*](gloss-w.md). Il est également possible de créer et de manipuler des classes et des instances CIM à l’aide [de l’API com pour WMI](com-api-for-wmi.md).

Un fournisseur WMI se compose normalement d’un fichier MOF, qui définit les classes de données et d’événements pour lesquelles le fournisseur retourne des données, ainsi qu’un fichier DLL qui contient le code qui fournit des données. Pour plus d’informations, consultez [fourniture de données à WMI](providing-data-to-wmi.md).

Les applications et les scripts du client WMI peuvent rechercher des instances de classes MOF du fournisseur ou s’abonner pour recevoir des notifications d’événements.

Vous pouvez effectuer les tâches suivantes avec MOF :

-   [Compilation des fichiers MOF](compiling-mof-files.md)
-   [Création d’une classe](creating-a-class.md)
-   [Création d’une instance](creating-an-instance.md)
-   [Création d’une méthode](creating-a-method.md)
-   [Ajout d’un qualificateur](adding-a-qualifier.md)
-   [Création d’un commentaire](creating-a-comment.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WMI](about-wmi.md)
</dt> </dl>

 

 



