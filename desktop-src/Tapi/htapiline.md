---
description: Le type de données HTAPILINE représente le descripteur TAPI opaque pour une structure de données de ligne.
ms.assetid: 732f0990-cbad-4ce0-873f-7b025603466e
title: HTAPILINE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80da6db2364b98647e542ece4b71aafd03f4fd9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527343"
---
# <a name="htapiline"></a><span data-ttu-id="83506-103">HTAPILINE</span><span class="sxs-lookup"><span data-stu-id="83506-103">HTAPILINE</span></span>

<span data-ttu-id="83506-104">Le type de données **HTAPILINE** représente le descripteur TAPI opaque pour une structure de données de ligne.</span><span class="sxs-lookup"><span data-stu-id="83506-104">The **HTAPILINE** datatype represents the TAPI opaque handle for a line data structure.</span></span> <span data-ttu-id="83506-105">L’interface TAPI doit résoudre une valeur de ce type en une référence à l’instance de structure de données appropriée.</span><span class="sxs-lookup"><span data-stu-id="83506-105">TAPI must resolve a value of this type into a reference to the appropriate data structure instance.</span></span> <span data-ttu-id="83506-106">Le fournisseur de services ne doit pas tenter de faire référence à ce comme s’il s’agissait d’un pointeur, faire des suppositions sur ses valeurs ou interpréter sa représentation de quelque façon que ce soit en passant sa valeur à l’interface TAPI aux moments opportuns.</span><span class="sxs-lookup"><span data-stu-id="83506-106">The service provider must not attempt to reference through this as if it were a pointer, make assumptions about its values, or interpret its representation in any way other than passing its value to TAPI at appropriate times.</span></span>

 

 



