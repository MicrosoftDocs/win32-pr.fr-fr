---
title: Configuration logicielle requise pour l’API WinSNMP
description: Une application WinSNMP doit accéder à l’API WinSNMP par le biais de la bibliothèque de liens dynamiques WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190728"
---
# <a name="software-requirements-for-the-winsnmp-api"></a><span data-ttu-id="de2ef-103">Configuration logicielle requise pour l’API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="de2ef-103">Software Requirements for the WinSNMP API</span></span>

<span data-ttu-id="de2ef-104">Une application WinSNMP doit accéder à l’API WinSNMP par le biais de la bibliothèque de liens dynamiques WSNMP32.DLL.</span><span class="sxs-lookup"><span data-stu-id="de2ef-104">A WinSNMP application must access the WinSNMP API through the dynamic-link library WSNMP32.DLL.</span></span>

<span data-ttu-id="de2ef-105">Les fichiers suivants sont requis pour prendre en charge les fonctionnalités de l’API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="de2ef-105">The following files are required to support the functionality of the WinSNMP API.</span></span>



| <span data-ttu-id="de2ef-106">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="de2ef-106">Filename</span></span>     | <span data-ttu-id="de2ef-107">Description</span><span class="sxs-lookup"><span data-stu-id="de2ef-107">Description</span></span>                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="de2ef-108">WSNMP32. LIB</span><span class="sxs-lookup"><span data-stu-id="de2ef-108">WSNMP32.LIB</span></span>  | <span data-ttu-id="de2ef-109">Bibliothèque WinSNMP</span><span class="sxs-lookup"><span data-stu-id="de2ef-109">WinSNMP Library</span></span>                                                                              |
| <span data-ttu-id="de2ef-110">WSNMP32.DLL</span><span class="sxs-lookup"><span data-stu-id="de2ef-110">WSNMP32.DLL</span></span>  | <span data-ttu-id="de2ef-111">Fournit l’interface WinSNMP</span><span class="sxs-lookup"><span data-stu-id="de2ef-111">Provides WinSNMP interface</span></span>                                                                   |
| <span data-ttu-id="de2ef-112">WINSNMP. Manutention</span><span class="sxs-lookup"><span data-stu-id="de2ef-112">WINSNMP.H</span></span>    | <span data-ttu-id="de2ef-113">Fichier d’en-tête WinSNMP</span><span class="sxs-lookup"><span data-stu-id="de2ef-113">WinSNMP header file</span></span>                                                                          |
| <span data-ttu-id="de2ef-114">SNMPTRAP.EXE</span><span class="sxs-lookup"><span data-stu-id="de2ef-114">SNMPTRAP.EXE</span></span> | <span data-ttu-id="de2ef-115">Reçoit des interruptions SNMP et les transfère à MGMTAPI.DLL, la bibliothèque API du Gestionnaire Microsoft SNMP</span><span class="sxs-lookup"><span data-stu-id="de2ef-115">Receives SNMP traps and forwards them to MGMTAPI.DLL, the Microsoft SNMP Manager API library</span></span> |
| <span data-ttu-id="de2ef-116">SNMPAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="de2ef-116">SNMPAPI.DLL</span></span>  | <span data-ttu-id="de2ef-117">Fournit des utilitaires SNMP</span><span class="sxs-lookup"><span data-stu-id="de2ef-117">Provides SNMP utilities</span></span>                                                                      |



 

 

 




