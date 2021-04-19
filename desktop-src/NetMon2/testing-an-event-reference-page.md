---
description: La dernière étape de la création d’une page de référence des événements consiste à la tester.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Test d’une page de référence d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531669"
---
# <a name="testing-an-event-reference-page"></a>Test d’une page de référence d’événement

La dernière étape de la création d’une page de référence des événements consiste à la tester. Vous pouvez tester un ERP en consultant le fichier dans un navigateur HTML, tel que Microsoft Internet Explorer. Vous pouvez installer l’ERP et sa DLL d’expert pour le tester pour l’appel d’événement et l’afficher dans le observateur d’événements Moniteur réseau.

## <a name="viewing-erps-that-have-no-dll"></a>Affichage des vos solutions ERP qui n’ont pas de DLL

Pour afficher l’ERP terminé sans DLL d’expert installée, ouvrez le fichier avec une visionneuse HTML qui prend en charge vos sources incorporées. L’illustration suivante montre l’exemple de fichier ERP décrit dans [écriture d’une ERP](writing-an-event-reference-page.md) telle qu’elle est affichée à l’aide de Microsoft Internet Explorer version 4,01.

![exemple de fichier ERP](images/ie-erp.png)

Test des vos solutions ERP qui ont une DLL

Une fois les fichiers ERP et la dll d' [**expert**](experts.md) créés, vous pouvez tester la fonctionnalité complète de votre vos solutions erp avec moniteur réseau. Il est supposé que la DLL est déboguée et peut générer des événements valides.

**Pour tester des vos solutions ERP qui ont une DLL**

1.  Vérifiez que la DLL d’expert appropriée est installée dans le répertoire approprié. Pour plus d’informations, consultez [installation d’un expert sur Moniteur réseau 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Vérifiez le [nom correct](naming-an-event-reference-page.md) du fichier ERP.
3.  Vérifiez l' [emplacement correct](installing-existing-erps-to-network-monitor-2-1.md) du vos solutions ERP dans le répertoire Moniteur réseau.
4.  Test d’expert vos solutions ERP dans l’interface utilisateur Moniteur réseau.
5.  Générez un événement de test.
6.  Vérifiez que l’ERP s’affiche dans le observateur d’événements Moniteur réseau.

Pour plus d’informations sur la création d’une ERP, consultez :

-   [Création d’un expert et surveillance des pages de référence des événements](creating-expert-and-monitor-event-reference-pages.md)
-   [Écriture d’une page de référence d’événement](writing-an-event-reference-page.md)
-   [Attribution d’un nom à une page de référence d’événement](naming-an-event-reference-page.md)

 

 



