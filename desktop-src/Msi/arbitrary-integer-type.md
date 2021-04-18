---
description: Le type d’entier arbitraire du type sémantique est l’un des types de format d’entier.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Type d’entier arbitraire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115378"
---
# <a name="arbitrary-integer-type"></a><span data-ttu-id="8b74e-103">Type d’entier arbitraire</span><span class="sxs-lookup"><span data-stu-id="8b74e-103">Arbitrary Integer Type</span></span>

<span data-ttu-id="8b74e-104">Le type d’entier arbitraire du [type sémantique](semantic-types.md) est l’un des [types de format d’entier](integer-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="8b74e-104">The Arbitrary Integer Type of [semantic type](semantic-types.md) is one of the [Integer Format Types](integer-format-types.md).</span></span> <span data-ttu-id="8b74e-105">Ce type d’élément configurable est un entier fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8b74e-105">This type of configurable item is an integer provided by the user.</span></span> <span data-ttu-id="8b74e-106">L’outil de fusion remplace cet entier dans les modèles spécifiés dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="8b74e-106">The merge tool substitutes this integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

<span data-ttu-id="8b74e-107">Pour spécifier un élément configurable de ce type, les auteurs du module doivent entrer le nom de la chaîne de texte dans la colonne nom, entrer « 2 » dans la colonne format et laisser vides les colonnes type et ContextData de la [table ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="8b74e-107">To specify a configurable item of this type, module authors should enter the name of the text string into the Name column, enter "2" into the Format column, and leave blank the Type and ContextData columns of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="8b74e-108">Les colonnes type et ContextData sont réservées et doivent avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="8b74e-108">The Type and ContextData columns are reserved and must be null.</span></span>

 

 



