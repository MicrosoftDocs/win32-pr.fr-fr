---
title: Chaînes de style C
description: Une application WinSNMP peut utiliser des chaînes de style C se terminant par un caractère NULL pour convertir des objets d’entité et d’identificateur d’objet (OID) vers et à partir de leurs représentations sous forme de chaîne.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839098"
---
# <a name="c-style-strings"></a><span data-ttu-id="8b163-103">Chaînes de style C</span><span class="sxs-lookup"><span data-stu-id="8b163-103">C-Style Strings</span></span>

<span data-ttu-id="8b163-104">Une application WinSNMP peut utiliser des chaînes de style C se terminant par un caractère **null** pour convertir des objets d’entité et d’identificateur d’objet (OID) vers et à partir de leurs représentations sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="8b163-104">A WinSNMP application can use **NULL**-terminated C-style strings to convert entity and object identifier (OID) objects to and from their string representations.</span></span>

<span data-ttu-id="8b163-105">Les fonctions WinSNMP qui manipulent des chaînes de style C incluent [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)et [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span><span class="sxs-lookup"><span data-stu-id="8b163-105">The WinSNMP functions that manipulate C-style strings include [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid), and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span></span> <span data-ttu-id="8b163-106">Étant donné que [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) et [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) retournent un pointeur vers une variable de chaîne de style C, l’application WinSNMP doit passer une valeur appropriée dans le paramètre *Size* lorsqu’il effectue des appels à ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="8b163-106">Because [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) return a pointer to a C-style string variable, the WinSNMP application must pass an appropriate value in the *size* parameter when it makes calls to these functions.</span></span> <span data-ttu-id="8b163-107">Pour plus d’informations, consultez les pages de référence de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="8b163-107">For more information, see the reference pages for these functions.</span></span>

> [!Note]  
> <span data-ttu-id="8b163-108">Le paramètre *Context* des fonctions [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) et [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) doit être une structure de chaîne d’octets, c’est-à-dire une structure [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) .</span><span class="sxs-lookup"><span data-stu-id="8b163-108">The *context* parameter of the [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) and [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) functions must be an octet string structure, that is, an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure.</span></span> <span data-ttu-id="8b163-109">Le paramètre de *contexte* ne peut pas être une chaîne de style C.</span><span class="sxs-lookup"><span data-stu-id="8b163-109">The *context* parameter cannot be a C-style string.</span></span> <span data-ttu-id="8b163-110">La chaîne contenue dans une structure **smiOCTETS** ne nécessite pas d’octet de fin **null**.</span><span class="sxs-lookup"><span data-stu-id="8b163-110">The string contained in an **smiOCTETS** structure does not require a **NULL**-terminating byte.</span></span>

 

 

 




