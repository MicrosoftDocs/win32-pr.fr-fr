---
title: Implémentation et activation d’un gestionnaire sans données de serveur supplémentaires
description: Implémentation et activation d’un gestionnaire sans données de serveur supplémentaires
ms.assetid: 9d91260a-4cec-4a10-bb57-d02999efae47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81df2bcaf1b50a0727127c4008d9763b76e05e4f2a5d80bf4b282bbbe02e5bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070856"
---
# <a name="implementing-and-activating-a-handler-with-no-extra-server-data"></a>Implémentation et activation d’un gestionnaire sans données de serveur supplémentaires

Pour créer une instance de votre gestionnaire, si ce n’est pas le cas, le serveur doit implémenter [**IStdMarshalInfo**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) mais pas [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). **IStdMarshalInfo** possède une méthode, [**GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler), qui récupère le CLSID du gestionnaire d’objets à utiliser dans le processus de destination. COM appelle cela quand il appelle [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) pour vous et active le gestionnaire côté client.

Ensuite, les implémentations du serveur et du gestionnaire doivent appeler la fonction [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) . Cette fonction crée un marshaleur standard sur chaque côté (appelé gestionnaire proxy côté client et un gestionnaire de stub côté serveur).

Le serveur appelle [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), en passant l’indicateur \_ Server SMEXF. Cela crée un marshaleur standard côté serveur (gestionnaire stub). La structure côté serveur est présentée dans l’illustration suivante :

![Diagramme qui montre la structure côté serveur.](images/b47b3bc0-3e7d-4be4-9767-7ae436bd1b21.png)

## <a name="server-side-structure"></a>Structure Server-Side

Le gestionnaire appelle [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), en passant le gestionnaire d’indicateurs SMEXF \_ . Cela crée un marshaleur standard côté client (gestionnaire proxy) et l’agrège avec le gestionnaire côté client. La durée de vie des deux sont gérées par l’objet d’identité de contrôle (implémentation d' [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)) que le système implémente lorsque le gestionnaire appelle **CoGetStdMarshalEx**. La structure côté client est représentée dans l’illustration suivante.

![Diagramme qui montre la structure côté client.](images/24ae70ef-dfa8-4784-90ac-dc6cfb043ee5.png)

## <a name="client-side-structure"></a>Structure Client-Side

Comme indiqué dans l’illustration précédente, le gestionnaire est en fait sandwich entre le gestionnaire proxy et l’identité/le contrôle inconnu. Cela permet au système de contrôler la durée de vie de l’objet tout en donnant au gestionnaire le contrôle sur les interfaces exposées. La ligne en pointillés entre l’identité et le gestionnaire proxy indique que les deux partagent une étroite intégration via des interfaces privées internes.

Quand COM appelle [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) pour le client, il crée l’instance de gestionnaire, en l’agrégeant avec l’identité. Le gestionnaire crée le marshaleur standard (par le biais de l’appel à [**CoGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex), en passant le contrôle inconnu qu’il a reçu lors de sa création). Le gestionnaire n’implémente pas [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , mais retourne simplement **IMarshal** à partir du marshaleur standard. Même si le gestionnaire implémente **IMarshal**, il n’est pas appelé pendant un démarshaleur.

Si deux threads démarshalent simultanément le même objet pour la première fois, il est possible que deux gestionnaires soient créés temporairement. Une version sera publiée par la suite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de Client-Side léger](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 