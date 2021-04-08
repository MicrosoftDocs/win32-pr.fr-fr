---
title: Obtention d’un ID de lien
description: À compter de Windows Server 2003, il n’est plus nécessaire de demander un linkID de Microsoft ; Il existe un processus pour générer automatiquement un linkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Obtention d’un ID de lien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101440"
---
# <a name="obtaining-a-link-id"></a>Obtention d’un ID de lien

À compter de Windows Server 2003, il n’est plus nécessaire de demander un [**LinkId**](/windows/desktop/ADSchema/a-linkid) de Microsoft ; Il existe un processus pour générer automatiquement un **LinkId**. Le système génère automatiquement un ID de lien pour un nouvel attribut lié lorsque l’attribut **LinkId** de l’attribut a la valeur 1.2.840.113556.1.2.50. Pour créer un lien précédent pour ce lien suivant, affectez au paramètre **LinkId** la valeur [**AttributeID**](/windows/desktop/ADSchema/a-attributeid) ou [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) du lien suivant. Le cache de schéma doit être rechargé après la création du lien suivant et avant la création du lien précédent. Dans le cas contraire, l' **AttributeID** ou le **ldapDisplayName** du lien Forward ne sera pas trouvé lors de la création du lien précédent. Le cache de schéma est rechargé à la demande, quelques minutes après qu’une modification de schéma a été effectuée ou lorsque le contrôleur de périphérique est redémarré. Créez tous les liens de transfert, rechargez le cache de schéma, puis créez tous les liens de retour.

Par exemple, lorsque vous avez créé les nouveaux attributs **myForwardLinkAttr** et **myBackLinkAttr**, et que vous souhaitez les lier :

> [!Note]  
> Dans cet exemple, les OID sont fictif. Consultez [obtention d’un identificateur d’objet auprès de Microsoft](obtaining-an-object-identifier-from-microsoft.md) pour obtenir des instructions sur l’obtention d’OID pour les nouveaux attributs.

 

1.  Définissez ces attributs sur l’attribut qui doit être le lien suivant :
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  Rechargez le schéma.
3.  Définissez ces attributs sur l’attribut qui doit être le lien précédent :
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs liés](linked-attributes.md)
</dt> <dt>

[Comment étendre le schéma](how-to-extend-the-schema.md)
</dt> </dl>

 

 