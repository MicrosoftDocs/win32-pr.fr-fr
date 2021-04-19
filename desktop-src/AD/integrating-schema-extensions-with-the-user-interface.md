---
title: Intégration des extensions de schéma avec l’interface utilisateur
description: Les outils d’administration de Active Directory Domain Services utilisent une architecture commune pour connecter l’interface utilisateur d’administration au schéma d’annuaire.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106544012"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a><span data-ttu-id="9a19b-103">Intégration des extensions de schéma avec l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="9a19b-103">Integrating Schema Extensions with the User Interface</span></span>

<span data-ttu-id="9a19b-104">Les outils d’administration de Active Directory Domain Services utilisent une architecture commune pour connecter l’interface utilisateur d’administration au schéma d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="9a19b-104">The administration tools of Active Directory Domain Services use a common architecture for connecting the administrative user interface to the directory schema.</span></span> <span data-ttu-id="9a19b-105">La pièce maîtresse de cette architecture est la classe d’objets **displaySpecifier** .</span><span class="sxs-lookup"><span data-stu-id="9a19b-105">The centerpiece of this architecture is the **displaySpecifier** object class.</span></span> <span data-ttu-id="9a19b-106">Les spécificateurs d’affichage et leur utilisation sont décrits en détail dans [extension de l’interface utilisateur pour les objets d’annuaire](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9a19b-106">Display specifiers and their usage are described in detail in [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

<span data-ttu-id="9a19b-107">Quand vous créez une classe en sous-classant une classe existante, vous pouvez tirer parti de l’interface utilisateur existante pour la superclasse en copiant le spécificateur d’affichage de la superclasse.</span><span class="sxs-lookup"><span data-stu-id="9a19b-107">When you create a new class by subclassing an existing class, you can leverage the existing UI for the superclass by copying the superclass' display specifier.</span></span> <span data-ttu-id="9a19b-108">Un moyen simple de copier le spécificateur d’affichage d’une classe consiste à l’exporter dans un fichier LDIF à l’aide de LDIFDE, de modifier le nom unique et le CN, puis d’importer le fichier LDIF modifié.</span><span class="sxs-lookup"><span data-stu-id="9a19b-108">An easy way to copy the display specifier for a class is to export it into an LDIF file using LDIFDE, edit the Distinguished name and CN, then import the modified LDIF file.</span></span> <span data-ttu-id="9a19b-109">Si la sous-classe possède des attributs supplémentaires, vous devrez fournir des pages de propriétés supplémentaires pour prendre en charge la modification.</span><span class="sxs-lookup"><span data-stu-id="9a19b-109">If the subclass has additional attributes, you will need to provide additional property pages to support editing.</span></span> <span data-ttu-id="9a19b-110">Si la sous-classe a des propriétés requises supplémentaires, vous devrez fournir des pages d’extension de boîte de dialogue de création, car l’interface utilisateur fournie par la superclasse n’a aucun moyen de créer ces nouveaux attributs.</span><span class="sxs-lookup"><span data-stu-id="9a19b-110">If the subclass has additional must-have properties, you will need to provide Creation Dialog extension pages since the UI provided by the superclass has no way to create these new attributes.</span></span>

 

 




