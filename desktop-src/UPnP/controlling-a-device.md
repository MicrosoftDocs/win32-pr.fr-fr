---
title: Contrôle d’un appareil
description: Une fois que vous avez découvert des appareils, vous pouvez les contrôler.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79d6e6993794a4af972af8538b9b1cd56902c34596197836990028b2761ffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656068"
---
# <a name="controlling-a-device"></a>Contrôle d’un appareil

Une fois que vous avez découvert des appareils, vous pouvez les contrôler.

**Pour afficher les propriétés d’un appareil**

1.  Sélectionnez un appareil dans la liste **appareils trouvés** .
2.  Cliquez sur Propriétés de l' **appareil**. La fenêtre Propriétés de l' **appareil** s’affiche avec les informations demandées.

> [!Note]  
> La fonctionnalité de présentation de la **vue** n’est pas disponible dans l’exemple de code C++.

 

**Pour afficher la page de présentation d’un appareil**

1.  Sélectionnez un appareil dans la liste **appareils trouvés** .
2.  Cliquez sur **afficher la présentation**. Une fenêtre Internet Explorer s’affiche avec la page de présentation demandée.

> [!Note]  
> **Description du service d’affichage.** la fonctionnalité n’est pas disponible dans l’exemple de code C++.

 

**Pour afficher une description de service**

1.  Vous pouvez entrer l’URL de la description de service dans le **service DESC. Champ URL** .

    ![URL de description du service](images/ucp-url.png)

2.  Cliquez sur **afficher le service DESC.** La fenêtre **visionneuse de description de service** s’affiche. Vous pouvez ensuite parcourir la description du service à l’aide de l’arborescence. Cette fonctionnalité n’est pas disponible dans l’exemple de code C++.

    ![fenêtre visionneuse de description de service](images/ucp-serv.png)

    Vous pouvez utiliser cinq commandes dans la fenêtre visionneuse de description de service.



| Bouton                 | Action effectuée                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Go                     | Charge le fichier affiché dans la **Description du service. Champ URL** .                                                                                                                              |
| Définir l’action             | Sélectionnez un nom d’action dans l’arborescence Description du service, puis cliquez sur **définir l’action**. Le nom de l’action est entré dans le champ **appeler l’action** de la fenêtre principale **UCP générique** .       |
| Set Variable           | Sélectionnez un nom de variable dans l’arborescence Description du service, puis cliquez sur **définir la variable**. Le nom de la variable est entré dans le champ **variable de requête** de la fenêtre principale **UCP générique** . |
| Remplir la liste des variables | Charge tous les noms de variable du service dans la liste des **variables de requête** de la fenêtre principale **UCP générique** .                                                                           |
| Remplir la liste d’actions   | Charge tous les noms d’action du service dans la liste d' **actions d’appel** de la fenêtre principale **UCP générique** .                                                                              |



 

**Pour contrôler un appareil**

1.  Dans la liste **appareils trouvés** , sélectionnez l’appareil que vous souhaitez contrôler.
2.  Dans la liste **choisir un service** , sélectionnez le service que vous souhaitez appeler ou la variable d’État que vous souhaitez interroger.

    ![fenêtre appareils de contrôle](images/ucp-contr.png)

    > [!Note]  
    > Le contenu de la **liste des services** est basé sur le périphérique sélectionné dans la liste **appareils trouvés** .

     

3.  Si vous souhaitez déterminer la valeur d’une variable d’État pour le service sélectionné, entrez le nom de la variable dans le champ de **variable de requête** pour le service. Cliquez sur **Requête**. Les résultats sont affichés dans le champ valeur de l’état de la **requête/arguments d’action out** .
4.  Si vous souhaitez appeler une action pour un service, entrez le nom de l’action dans le champ **appeler l’action** , ainsi que tous les arguments dans le champ arguments de l' **action** . Cliquez sur **appeler**. Les résultats sont affichés dans le champ valeur de l’état de la **requête/arguments de l’action out** , le cas échéant.

    La valeur de retour, le cas échéant, est contenue dans le premier argument out.

    > [!Note]  
    > S’il existe plusieurs arguments pour une action, séparez-les par des espaces.

     

5.  Affichez les informations sur les événements dans le champ **événements** pour le service sélectionné.

 

 




