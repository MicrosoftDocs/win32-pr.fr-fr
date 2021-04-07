---
title: Prise en charge des chaînes d’adresses IPX dans WinSNMP
description: WinSNMP 2,0 formalise l’utilisation des chaînes d’adresses IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671074"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a><span data-ttu-id="cdfd1-103">Prise en charge des chaînes d’adresses IPX dans WinSNMP</span><span class="sxs-lookup"><span data-stu-id="cdfd1-103">Support for IPX Address Strings in WinSNMP</span></span>

<span data-ttu-id="cdfd1-104">WinSNMP 2,0 formalise l’utilisation des chaînes d’adresses IPX.</span><span class="sxs-lookup"><span data-stu-id="cdfd1-104">WinSNMP 2.0 formalizes the use of IPX address strings.</span></span> <span data-ttu-id="cdfd1-105">Si vous spécifiez une chaîne d’adresse IPX comme paramètre d’entrée de la fonction [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) , vous devez mettre en forme la chaîne en utilisant les normes suivantes :</span><span class="sxs-lookup"><span data-stu-id="cdfd1-105">If you specify an IPX address string as an input parameter to the [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) function, you must format the string using the following standards:</span></span>

-   <span data-ttu-id="cdfd1-106">Numéro de réseau composé de huit chiffres hexadécimaux (rempli à zéro si nécessaire)</span><span class="sxs-lookup"><span data-stu-id="cdfd1-106">A network number that consists of eight hexadecimal digits (zero-filled if necessary)</span></span>
-   <span data-ttu-id="cdfd1-107">Séparateur («  : », « . » ou « – »)</span><span class="sxs-lookup"><span data-stu-id="cdfd1-107">A separator (either ":", "." or " – ")</span></span>
-   <span data-ttu-id="cdfd1-108">Numéro de nœud composé de 12 chiffres hexadécimaux (rempli à zéro si nécessaire)</span><span class="sxs-lookup"><span data-stu-id="cdfd1-108">A node number that consists of 12 hexadecimal digits (zero-filled if necessary)</span></span>

<span data-ttu-id="cdfd1-109">Par exemple, 00000001:00081A0D01C2 ou 00000001.00081 a0d01c2.</span><span class="sxs-lookup"><span data-stu-id="cdfd1-109">For example, 00000001:00081A0D01C2 or 00000001.00081a0d01c2.</span></span> <span data-ttu-id="cdfd1-110">Les chiffres hexadécimaux peuvent être en majuscules ou en minuscules.</span><span class="sxs-lookup"><span data-stu-id="cdfd1-110">Hexadecimal digits can be uppercase or lowercase.</span></span>

<span data-ttu-id="cdfd1-111">Il s’agit du format utilisé par la fonction [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) pour retourner une chaîne d’adresse IPX.</span><span class="sxs-lookup"><span data-stu-id="cdfd1-111">This is the format the [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) function uses to return an IPX address string.</span></span> <span data-ttu-id="cdfd1-112">La chaîne est retournée lorsqu’une application qui fonctionne dans l’un des modes SNMPAPI non \_ traduits appelle la fonction **SnmpEntityToStr** .</span><span class="sxs-lookup"><span data-stu-id="cdfd1-112">The string is returned when an application that is operating in one of the SNMPAPI\_UNTRANSLATED modes calls the **SnmpEntityToStr** function.</span></span> <span data-ttu-id="cdfd1-113">La chaîne peut également être retournée lorsque l’application fonctionne en \_ mode de traduction SNMPAPI et qu’aucun nom convivial n’est disponible pour l’entité.</span><span class="sxs-lookup"><span data-stu-id="cdfd1-113">The string can also be returned when the application is operating in SNMPAPI\_TRANSLATED mode and no user-friendly name is available for the entity.</span></span>

 

 




