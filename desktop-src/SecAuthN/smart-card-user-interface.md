---
description: L’interface utilisateur de la carte à puce est une boîte de dialogue commune unique qui permet à l’utilisateur de spécifier ou de rechercher une carte à puce pour l’ouvrir (c’est-à-dire, se connecter à une application et l’utiliser dans une application).
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Interface utilisateur de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536396"
---
# <a name="smart-card-user-interface"></a>Interface utilisateur de carte à puce

L' [*interface utilisateur*](../secgloss/u-gly.md) de la carte à puce est une [*boîte de dialogue commune*](../secgloss/s-gly.md) unique qui permet à l’utilisateur de spécifier ou de rechercher une carte à puce pour l’ouvrir (c’est-à-dire, se connecter à une application et l’utiliser dans une application).

Voici deux façons d’utiliser la boîte de dialogue commune. Les deux partent du principe que l’interface utilisateur de la boîte de dialogue s’affiche. Pour plus d’informations, consultez [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).

**Pour sélectionner une carte à puce à ouvrir**

1.  Déclarez une variable de type **OPENCARDNAME**.
2.  Fournissez suffisamment d’informations dans la boîte de dialogue commune pour affiner la recherche d’une carte à puce recherchée par l’application appelante. Cela comprend la spécification de **lpstrGroupNames**, **lpstrCardNames** et **rgguidInterfaces**. Cela implique également la spécification d’un mode de partage et d’un protocole préférés à utiliser lorsque la boîte de dialogue commune se connecte à la carte à l’aide des membres **dwShareMode** et **dwPreferredProtocols** de la structure [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) .
3.  Appelez la fonction [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) pour afficher la boîte de dialogue commune à l’utilisateur. Une ligne d’informations d’aide simple s’affiche, et si l’une des cartes demandées est trouvée, la carte est mise en surbrillance dans l’affichage. Pour les recherches sur plusieurs noms de carte, le premier lecteur qui contient l’une des cartes préférées est mis en surbrillance.
4.  L’utilisateur sélectionne ensuite une carte, clique sur **OK** et se connecte à la carte à puce.

**Pour rechercher une carte spécifique**

1.  Déclarez une variable de type **OPENCARDNAME**.
2.  Fournissez suffisamment d’informations dans la boîte de dialogue commune pour affiner la recherche d’une carte à puce recherchée par l’application appelante. Cela comprend la spécification de **lpstrGroupNames**, **lpstrCardNames** et **rgguidInterfaces**.
3.  Créez les fonctions de rappel **Connect**, **Check** et **Disconnect** , puis définissez les membres de données **lpfnConnect**, **lpfnCheck** et **lpfnDisconnect** de manière appropriée.
    > [!Note]  
    > Les trois fonctions et membres doivent être disponibles lors de l’utilisation de la boîte de dialogue commune de cette façon.

     

4.  Appelez la fonction de boîte de dialogue commune [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) .
5.  La boîte de dialogue commune recherche les cartes demandées. Si un nom de carte ou une [*chaîne rar*](../secgloss/a-gly.md) correspondante est trouvé, les fonctions de rappel de **connexion**, de **vérification** et de **déconnexion** seront appelées dans l’ordre. Si une carte transmet la routine de **vérification** (c’est-à-dire que le rappel de **vérification** retourne la **valeur true**), cette carte est mise en surbrillance dans l’affichage de l’utilisateur.
    > [!Note]  
    > Si plusieurs noms de carte sont fournis, le premier lecteur qui contient l’une des cartes demandées et transmet la routine **Check** sera la carte sélectionnée.

     

6.  Si aucune correspondance n’est trouvée, une boîte de dialogue commune s’affiche.

 

 
