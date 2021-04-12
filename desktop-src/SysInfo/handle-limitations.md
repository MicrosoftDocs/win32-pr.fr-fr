---
description: Certains objets ne prennent en charge qu’un seul handle à la fois.
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: Limitations des handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210231"
---
# <a name="handle-limitations"></a><span data-ttu-id="2f4e6-103">Limitations des handles</span><span class="sxs-lookup"><span data-stu-id="2f4e6-103">Handle Limitations</span></span>

<span data-ttu-id="2f4e6-104">Certains objets ne prennent en charge qu’un seul handle à la fois.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-104">Some objects support only one handle at a time.</span></span> <span data-ttu-id="2f4e6-105">Le système fournit le descripteur lorsqu’une application crée l’objet et invalide le descripteur lorsque l’application détruit l’objet.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-105">The system provides the handle when an application creates the object and invalidates the handle when the application destroys the object.</span></span> <span data-ttu-id="2f4e6-106">Les autres objets prennent en charge plusieurs descripteurs sur un seul objet.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-106">Other objects support multiple handles to a single object.</span></span> <span data-ttu-id="2f4e6-107">Le système d’exploitation supprime automatiquement l’objet de la mémoire après la fermeture du dernier handle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-107">The operating system automatically removes the object from memory after the last handle to the object is closed.</span></span>

<span data-ttu-id="2f4e6-108">Le nombre total de handles ouverts dans le système est limité uniquement par la quantité de mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-108">The total number of open handles in the system is limited only by the amount of memory available.</span></span> <span data-ttu-id="2f4e6-109">Certains types d’objets prennent en charge un nombre limité de handles par session ou par processus.</span><span class="sxs-lookup"><span data-stu-id="2f4e6-109">Some object types support a limited number of handles per session or per process.</span></span>

 

 



