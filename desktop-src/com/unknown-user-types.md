---
title: Types d’utilisateurs inconnus
description: Types d’utilisateurs inconnus
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363552"
---
# <a name="unknown-user-types"></a>Types d’utilisateurs inconnus

Vous pouvez faciliter la localisation du produit en ajoutant la clé de Registre suivante :

**HKEY \_ \_Ordinateurs locaux \\ logiciel \\ Microsoft \\ OLE2** \\ **UnknownUserType**  =  *usertype*

Cette clé permet aux fonctions de retourner une chaîne spécifiée plutôt qu’une valeur par défaut « Unknown », ce qui permet aux localisateurs de spécifier un type d’utilisateur d’une langue différente.

L’implémentation du gestionnaire par défaut COM de [**IOleObject :: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examine le registre en appelant [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype). Si la classe de l’objet est introuvable dans le registre, le type d’utilisateur de l’instance [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) de l’objet est retourné. Si la classe est introuvable dans l’instance **IStorage** de l’objet, la chaîne « Unknown » est retournée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des applications COM](registering-com-applications.md)
</dt> </dl>

 

 