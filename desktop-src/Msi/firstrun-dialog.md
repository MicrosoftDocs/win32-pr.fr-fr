---
description: Une séquence de la boîte de dialogue FirstRun collecte le nom d’utilisateur, le nom de la société et les informations d’ID du produit. Le programme d’installation vérifie l’ID de produit au cours de cette boîte de dialogue.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Boîte de dialogue FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201962"
---
# <a name="firstrun-dialog"></a><span data-ttu-id="f7bed-104">Boîte de dialogue FirstRun</span><span class="sxs-lookup"><span data-stu-id="f7bed-104">FirstRun Dialog</span></span>

<span data-ttu-id="f7bed-105">Une séquence de la boîte de dialogue FirstRun collecte le nom d’utilisateur, le nom de la société et les informations d’ID du produit.</span><span class="sxs-lookup"><span data-stu-id="f7bed-105">A FirstRun dialog box sequence collects user name, company name, and product ID information.</span></span> <span data-ttu-id="f7bed-106">Le programme d’installation vérifie l’ID de produit au cours de cette boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f7bed-106">The installer verifies the product ID during this dialog.</span></span>

<span data-ttu-id="f7bed-107">Une séquence de la boîte de dialogue FirstRun n’est généralement pas une partie de la séquence d’action et est appelée à la place par la fonction [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) lors de la première exécution du produit.</span><span class="sxs-lookup"><span data-stu-id="f7bed-107">A FirstRun dialog box sequence is usually not a part of the action sequence and is instead called by the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function on the first run of the product.</span></span>

<span data-ttu-id="f7bed-108">L’auteur d’un package d’installation peut utiliser la séquence de dialogue de modèle ou créer une séquence différente.</span><span class="sxs-lookup"><span data-stu-id="f7bed-108">An author of an installer package may use the template dialog sequence or create a different sequence.</span></span> <span data-ttu-id="f7bed-109">Toutefois, la séquence de dialogue doit définir les propriétés suivantes pour l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="f7bed-109">The dialog sequence however needs to have the user set the following properties:</span></span>

-   <span data-ttu-id="f7bed-110">Propriété [**username**](username.md)</span><span class="sxs-lookup"><span data-stu-id="f7bed-110">[**USERNAME**](username.md) property</span></span>
-   <span data-ttu-id="f7bed-111">[**CompanyName**](companyname.md) , propriété</span><span class="sxs-lookup"><span data-stu-id="f7bed-111">[**COMPANYNAME**](companyname.md) property</span></span>
-   <span data-ttu-id="f7bed-112">[**PIDKEY**](pidkey.md) , propriété</span><span class="sxs-lookup"><span data-stu-id="f7bed-112">[**PIDKEY**](pidkey.md) property</span></span>

<span data-ttu-id="f7bed-113">L’ID de produit est validé au cours de la boîte de dialogue à l’aide de l' [Action ValidateProductID](validateproductid-action.md) ou du [ControlEvent, ValidateProductID](validateproductid-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="f7bed-113">The product ID will be validated during the dialog using the [ValidateProductID action](validateproductid-action.md) or the [ValidateProductID ControlEvent](validateproductid-controlevent.md).</span></span>

<span data-ttu-id="f7bed-114">Si l’ID de produit est défini en tant que propriété sur la ligne de commande ou par une transformation, la nécessité d’avoir à nouveau l’ID de produit dans la boîte de dialogue de première exécution peut être contournée en contrôlant l’affichage à l’aide de la propriété [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="f7bed-114">If the product ID is set as a property on the command line, or by a transform, then the necessity of having the user reenter the product ID during the first-run dialog can be circumvented by controlling the display using the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="f7bed-115">Après la validation réussie de l’ID de produit, la propriété **ProductID** est définie sur l’ID de produit complet valide.</span><span class="sxs-lookup"><span data-stu-id="f7bed-115">Following the successful validation of the product ID the **ProductID** property is set to the full, valid product ID.</span></span>

 

 



