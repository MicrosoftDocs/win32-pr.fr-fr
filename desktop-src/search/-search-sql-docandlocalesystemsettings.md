---
description: Lorsque le système d’exploitation, ou même une application, est configuré pour utiliser une langue et des paramètres régionaux particuliers, de nombreux paramètres sont affectés.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Paramètres des paramètres régionaux du document et du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9408093a8583a4b17566b5fcd118b30439c0ebda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513369"
---
# <a name="document-and-system-locale-settings"></a><span data-ttu-id="5bda8-103">Paramètres des paramètres régionaux du document et du système</span><span class="sxs-lookup"><span data-stu-id="5bda8-103">Document and System Locale Settings</span></span>

<span data-ttu-id="5bda8-104">Lorsque le système d’exploitation, ou même une application, est configuré pour utiliser une langue et des paramètres régionaux particuliers, de nombreux paramètres sont affectés.</span><span class="sxs-lookup"><span data-stu-id="5bda8-104">When the operating system, or even an application, is set to use a particular language and locale, many settings are affected.</span></span> <span data-ttu-id="5bda8-105">Ces paramètres incluent le format numérique, le format de date, le format monétaire, le mappage en majuscules et en minuscules, l’ordre de tri du dictionnaire, la création de jetons et d’autres.</span><span class="sxs-lookup"><span data-stu-id="5bda8-105">These settings include numeric format, date format, currency format, uppercase and lowercase mapping, dictionary sort ordering, tokenization, and others.</span></span> <span data-ttu-id="5bda8-106">Bien que ces paramètres aident Windows Search à fournir une excellente prise en charge localisée, des résultats inattendus peuvent se produire lorsque des documents d’un paramètre régional sont recherchés à l’aide d’un système défini sur un autre paramètre régional.</span><span class="sxs-lookup"><span data-stu-id="5bda8-106">Although these settings help Windows Search provide excellent localized support, unexpected results can occur when documents from one locale are searched by using a system that is set to another locale.</span></span>

<span data-ttu-id="5bda8-107">Lorsque l’objet [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) traite les propriétés et le contenu de texte d’un document, il signale la langue de ce document à l’indexeur de contenu.</span><span class="sxs-lookup"><span data-stu-id="5bda8-107">When the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) object processes a document's text properties and content, it reports the language of that document to the content indexer.</span></span> <span data-ttu-id="5bda8-108">À l’aide de ces informations, Windows Search peut appliquer l’analyseur lexical approprié.</span><span class="sxs-lookup"><span data-stu-id="5bda8-108">Using this information, Windows Search can apply the appropriate word breaker.</span></span>

 

 
