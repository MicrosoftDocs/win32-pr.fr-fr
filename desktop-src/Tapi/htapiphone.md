---
description: Le type de données HTAPIPHONE représente un descripteur opaque TAPIs pour une structure de données de téléphone.
ms.assetid: e869cb3e-0eeb-4edf-a272-a655a236a3a2
title: HTAPIPHONE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94706270b1148166181eda0d8df9b940c269f62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524505"
---
# <a name="htapiphone"></a><span data-ttu-id="8d22f-103">HTAPIPHONE</span><span class="sxs-lookup"><span data-stu-id="8d22f-103">HTAPIPHONE</span></span>

<span data-ttu-id="8d22f-104">Le type de données **HTAPIPHONE** représente le descripteur opaque de l’interface TAPI pour une structure de données de téléphone.</span><span class="sxs-lookup"><span data-stu-id="8d22f-104">The **HTAPIPHONE** datatype represents TAPI's opaque handle for a phone data structure.</span></span> <span data-ttu-id="8d22f-105">L’interface TAPI doit résoudre une valeur de ce type en une référence à l’instance de structure de données appropriée.</span><span class="sxs-lookup"><span data-stu-id="8d22f-105">TAPI must resolve a value of this type into a reference to the appropriate data structure instance.</span></span> <span data-ttu-id="8d22f-106">Le fournisseur de services ne doit pas tenter de faire référence à ce comme s’il s’agissait d’un pointeur, faire des suppositions sur ses valeurs ou interpréter sa représentation de quelque façon que ce soit en passant sa valeur à l’interface TAPI aux moments opportuns.</span><span class="sxs-lookup"><span data-stu-id="8d22f-106">The service provider must not attempt to reference through this as if it were a pointer, make assumptions about its values, or interpret its representation in any way other than passing its value to TAPI at appropriate times.</span></span>

 

 



