---
description: Objets d’activation
ms.assetid: 767d5f1c-2b8d-43b6-916b-035129e93204
title: Objets d’activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8741cbfa8bc3801a23b4976e60c0a3ad028b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113439"
---
# <a name="activation-objects"></a>Objets d’activation

Un *objet d’activation* est un objet d’assistance qui est utilisé pour créer un autre objet, quelque peu similaire à une fabrique de classe. Les objets d’activation exposent l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

Un objet d’activation vous permet de différer la création de l’objet cible, car vous pouvez conserver un pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) sans créer l’objet cible. Les objets d’activation peuvent également être sérialisés et, par conséquent, utilisés pour créer l’objet cible dans un autre processus. Par exemple, les objets d’activation sont utilisés pour marshaler des composants de pipeline à partir du processus d’application vers le processus PMP (Protected Media Path). Les objets d’activation sont également utilisés par certaines fonctions d’énumération qui retournent une liste de pointeurs **IMFActivate** . Avant de créer l’objet cible, l’application peut obtenir des informations sur l’objet en examinant les attributs de l’objet d’activation.

Pour créer l’objet cible à partir d’un objet d’activation, appelez la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) . L’appelant doit appeler [**IMFActivate :: ShutdownObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) lorsqu’il est terminé à l’aide de l’objet créé. Souvent, l’application crée l’objet d’activation et la session multimédia appelle **ActivateObject**. Dans ce cas, la session multimédia, et non l’application, doit appeler **ShutdownObject**. Dans d’autres situations, l’application reçoit un pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) à partir de la session multimédia, et l’application appelle **ActivateObject** et **ShutdownObject**. (Par exemple, consultez [Comment lire des fichiers multimédias protégés](how-to-play-protected-media-files.md).)

Les objets d’activation peuvent avoir des attributs, et l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) hérite de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Certains objets d’activation utilisent des attributs pour configurer l’objet créé. Les attributs spécifiques pris en charge par chaque objet sont documentés dans la référence de la fonction de création de cet objet d’activation. Définissez les attributs à l’aide du pointeur **IMFActivate** que vous recevez de la fonction.

Pour la lecture protégée, les objets d’activation sont marshalés vers le processus PMP. Pour prendre en charge le marshaling, un objet d’activation doit exposer l’interface **IPersistStream** . En outre, l’objet d’activation et l’objet créé doivent être des composants approuvés si le PMP s’exécute dans un processus protégé. Cela n’est pas obligatoire lorsque l’PMP est chargé dans un processus non protégé.

Pour utiliser un objet de pipeline personnalisé (tel qu’un récepteur multimédia) à l’intérieur du processus PMP, vous devez implémenter un objet d’activation pour votre objet de pipeline :

-   L’objet d’activation doit exposer [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) et **IPersistStream**.
-   La méthode **IPersist :: GetClassID** de l’objet d’activation doit retourner le CLSID de l’objet d’activation.
-   Si vous le souhaitez, vous pouvez implémenter les méthodes **IPersistStream :: Save** et **IPersistStream :: Load** pour marshaler les données dont vous avez besoin pour configurer votre objet d’activation.

Lorsque la session multimédia charge la topologie à l’intérieur du processus PMP, elle appelle **CoCreateInstance** pour créer une nouvelle instance de votre objet d’activation. Ensuite, il appelle [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pour créer l’objet de pipeline.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de plateforme Media Foundation](media-foundation-platform-apis.md)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> </dl>

 

 



