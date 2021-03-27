---
description: Chemins courbés
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Chemins courbés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863674"
---
# <a name="curved-paths"></a><span data-ttu-id="07ffb-103">Chemins courbés</span><span class="sxs-lookup"><span data-stu-id="07ffb-103">Curved Paths</span></span>

<span data-ttu-id="07ffb-104">Une application peut aplatir les courbes dans un chemin d’accès en appelant la fonction [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) .</span><span class="sxs-lookup"><span data-stu-id="07ffb-104">An application can flatten the curves in a path by calling the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function.</span></span> <span data-ttu-id="07ffb-105">Cette fonction est particulièrement utile pour les applications qui tiennent du texte sur le contour d’un tracé qui contient des courbes.</span><span class="sxs-lookup"><span data-stu-id="07ffb-105">This function is especially useful for applications that fit text onto the contour of a path which contains curves.</span></span> <span data-ttu-id="07ffb-106">Pour ajuster le texte, l’application doit effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="07ffb-106">To fit the text, the application must perform the following steps:</span></span>

1.  <span data-ttu-id="07ffb-107">Créez le chemin d’accès où le texte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="07ffb-107">Create the path where the text appears.</span></span>
2.  <span data-ttu-id="07ffb-108">Appelez la fonction [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) pour convertir les courbes d’un tracé en segments de ligne.</span><span class="sxs-lookup"><span data-stu-id="07ffb-108">Call the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function to convert the curves in a path into line segments.</span></span>
3.  <span data-ttu-id="07ffb-109">Appelez la fonction [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) pour récupérer ces segments de ligne.</span><span class="sxs-lookup"><span data-stu-id="07ffb-109">Call the [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) function to retrieve those line segments.</span></span>
4.  <span data-ttu-id="07ffb-110">Calculez la longueur de chaque ligne et la largeur de chaque caractère de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="07ffb-110">Calculate the length of each line and the width of each character in the string.</span></span>
5.  <span data-ttu-id="07ffb-111">Utilisez les données de largeur de ligne et de largeur de caractère pour positionner chaque caractère le long de la courbe.</span><span class="sxs-lookup"><span data-stu-id="07ffb-111">Use line-width and character-width data to position each character along the curve.</span></span>

 

 



