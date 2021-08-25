---
title: Configuration du service de noms
description: à compter de Windows 2000, lorsque vous installez le SDK Windows, le programme d’installation sélectionne automatiquement Microsoft Locator comme fournisseur de services de noms. Vous pouvez modifier le nom du fournisseur de services par le biais du panneau de configuration.
ms.assetid: bd72ca2f-bb93-4057-a877-be755a88719d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84450f4408ac0e90be04cfff7d1cbc92890cde4434969431a986e9cda378ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022439"
---
# <a name="configuring-the-name-service"></a>Configuration du service de noms

à compter de Windows 2000, lorsque vous installez le SDK Windows, le programme d’installation sélectionne automatiquement Microsoft Locator comme fournisseur de services de noms. Vous pouvez modifier le nom du fournisseur de services par le biais du panneau de configuration.

L’ordinateur hôte qui exécute le NSID joue le rôle de passerelle vers le service d’annuaire de cellules/service d’annuaires de cellules DCE, en passant les appels de fonction NSI entre les ordinateurs qui exécutent des systèmes d’exploitation Microsoft et des ordinateurs DCE. Une adresse réseau peut contenir jusqu’à 80 caractères, par exemple, 11.1.9.169 est une adresse valide.

> [!Note]  
> Vous devez disposer du produit CDS (Digital Equipment) DCE pour configurer les CDS DCE en tant que fournisseur de services de noms. Consultez la documentation fournie par Digital Equipment Corporation pour plus d’informations sur les CDS DCE.

 

**Pour reconfigurer le fournisseur de services de noms**

1.  Dans le panneau de configuration, cliquez sur l’icône **connexions réseau** . La fenêtre **connexions réseau** s’affiche.
2.  Sélectionnez la connexion réseau à configurer, cliquez avec le bouton droit, puis sélectionnez **Propriétés** dans le menu contextuel. La boîte de dialogue **Propriétés de connexion** s’affiche.
3.  Dans la boîte de dialogue **Propriétés de connexion** , sélectionnez **client pour les réseaux Microsoft** , puis cliquez sur le bouton **Propriétés** . La boîte **de dialogue Propriétés du client pour Microsoft Network** s’affiche.
4.  Dans la boîte de dialogue **Propriétés du client pour Microsoft Network** , ouvrez la liste déroulante **fournisseur de services de noms** et sélectionnez un fournisseur de noms dans la liste.
    1.  Lorsque vous sélectionnez Microsoft Locator, cliquez sur OK. Le processus de configuration est alors terminé.
    2.  Lorsque vous sélectionnez le service d’annuaire de cellules/service d’annuaires de cellules DCE, dans la zone **adresse réseau** , tapez le nom de l’ordinateur hôte qui exécute le démon NSI (NSID), puis cliquez sur OK.

**pour reconfigurer le fournisseur de services de noms pour Windows 2000**

1.  Dans le panneau de configuration, cliquez sur l’icône **réseau** .

    La boîte de dialogue **réseau** s’affiche.

2.  Dans la boîte de dialogue **réseau** , cliquez sur **configurer**.
3.  Dans la liste **NetworkSoftware** , sélectionnez **configuration RPC**.

    La boîte de dialogue **configuration du fournisseur de services de noms RPC** s’affiche.

4.  Dans la boîte de dialogue **configuration du fournisseur de services de noms RPC** , sélectionnez un fournisseur de services de noms dans la liste.
    1.  Lorsque vous sélectionnez Microsoft Locator, cliquez sur OK. Le processus de configuration est alors terminé.
    2.  Lorsque vous sélectionnez le service d’annuaire de cellules/service d’annuaires de cellules DCE, dans la zone **adresse réseau** , tapez le nom de l’ordinateur hôte qui exécute le démon NSI (NSID), puis cliquez sur OK.

 

 




