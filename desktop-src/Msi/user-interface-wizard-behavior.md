---
description: Pour créer une interface utilisateur simple, les développeurs de packages d’installation peuvent utiliser une conception d’interface utilisateur qui respecte le comportement de l’Assistant Interface.
ms.assetid: c69ba452-3c2e-47d7-8ea0-8f8f9e6b58c8
title: Comportement de l’Assistant interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045aa59fe510ff10f428d0a7c74549ce4d817157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760138"
---
# <a name="user-interface-wizard-behavior"></a><span data-ttu-id="2dde3-103">Comportement de l’Assistant interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="2dde3-103">User Interface Wizard Behavior</span></span>

<span data-ttu-id="2dde3-104">Pour créer une interface utilisateur simple, les développeurs de packages d’installation peuvent utiliser une conception d’interface utilisateur qui respecte le comportement de l’Assistant Interface.</span><span class="sxs-lookup"><span data-stu-id="2dde3-104">To author a simple user interface, developers of installation packages can utilize a user interface design that adheres to interface wizard behavior.</span></span>

<span data-ttu-id="2dde3-105">Le terme comportement de l’Assistant de l’interface utilisateur signifie que chaque boîte de dialogue d’une séquence contient un bouton de **>>suivant** , sur lequel l’utilisateur clique pour passer à la boîte de dialogue suivante après avoir entré des données ou configuré des informations dans la boîte de dialogue active.</span><span class="sxs-lookup"><span data-stu-id="2dde3-105">The term user interface wizard behavior means that each dialog box in a sequence contains a **Next>>** button, which the user clicks to move to the next dialog box after entering data or configuring information in the current dialog box.</span></span> <span data-ttu-id="2dde3-106">Si l’utilisateur décide de revenir en arrière et de modifier les informations entrées dans une boîte de dialogue précédente, chaque boîte de dialogue contient un bouton **<<précédent** sur lequel l’utilisateur clique pour revenir en arrière.</span><span class="sxs-lookup"><span data-stu-id="2dde3-106">If the user decides to go back and change any information entered in a previous dialog box, each dialog box contains a **<<Previous** button that the user clicks to go back.</span></span> <span data-ttu-id="2dde3-107">À la fin de la séquence de l’Assistant, l’utilisateur clique sur un bouton **Terminer** pour commencer le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="2dde3-107">At the end of the wizard sequence, the user clicks a **Finish** button to begin the installation process.</span></span>

<span data-ttu-id="2dde3-108">L’interface utilisateur décrite dans l’exemple d’interface utilisateur adhère au comportement de l’Assistant interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2dde3-108">The UI described in the UI example adheres to user interface wizard behavior.</span></span> <span data-ttu-id="2dde3-109">Consultez [un exemple d’installation](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="2dde3-109">See [An Installation Example](an-installation-example.md).</span></span>

 

 



