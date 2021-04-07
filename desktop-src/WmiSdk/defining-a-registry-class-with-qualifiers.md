---
description: Les classes utilisées pour contenir les données de Registre sont définies avec plusieurs qualificateurs standard.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Définition d’une classe Registry avec des qualificateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864026"
---
# <a name="defining-a-registry-class-with-qualifiers"></a><span data-ttu-id="65458-103">Définition d’une classe Registry avec des qualificateurs</span><span class="sxs-lookup"><span data-stu-id="65458-103">Defining a Registry Class With Qualifiers</span></span>

<span data-ttu-id="65458-104">Les classes utilisées pour contenir les données de Registre sont définies avec plusieurs qualificateurs standard.</span><span class="sxs-lookup"><span data-stu-id="65458-104">The classes used to hold registry data are defined with several standard qualifiers.</span></span>

<span data-ttu-id="65458-105">La liste suivante répertorie les qualificateurs standard :</span><span class="sxs-lookup"><span data-stu-id="65458-105">The following is a list of the standard qualifiers:</span></span>

-   <span data-ttu-id="65458-106">[](standard-wmi-qualifiers.md) [ **Fournisseur** et dynamique](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="65458-106">[Dynamic](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>

    <span data-ttu-id="65458-107">Vous pouvez attacher le qualificateur **dynamique** à une classe ou à une instance.</span><span class="sxs-lookup"><span data-stu-id="65458-107">You can attach the **Dynamic** qualifier to either a class or an instance.</span></span> <span data-ttu-id="65458-108">Le qualificateur **dynamique** marque la classe ou l’instance comme gérée dynamiquement par un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="65458-108">The **Dynamic** qualifier marks the class or instance as managed dynamically by a provider.</span></span> <span data-ttu-id="65458-109">Lorsque **Dynamic** apparaît sur une classe ou une instance, le qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) doit également apparaître.</span><span class="sxs-lookup"><span data-stu-id="65458-109">When **Dynamic** appears on a class or instance, the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier must also appear.</span></span> <span data-ttu-id="65458-110">Le qualificateur du **fournisseur** identifie le fournisseur particulier qui doit gérer l’instance ou la classe dynamique.</span><span class="sxs-lookup"><span data-stu-id="65458-110">The **Provider** qualifier identifies the particular provider that must manage the dynamic class or instance.</span></span>

-   [<span data-ttu-id="65458-111">ClassContext</span><span class="sxs-lookup"><span data-stu-id="65458-111">ClassContext</span></span>](standard-wmi-qualifiers.md)

    <span data-ttu-id="65458-112">Le qualificateur **ClassContext** est attaché à une classe.</span><span class="sxs-lookup"><span data-stu-id="65458-112">The **ClassContext** qualifier is attached to a class.</span></span> <span data-ttu-id="65458-113">Il spécifie le chemin d’accès à la clé de Registre qui contient les informations que la classe représente.</span><span class="sxs-lookup"><span data-stu-id="65458-113">It specifies the path to the registry key that contains the information the class represents.</span></span>

    <span data-ttu-id="65458-114">Le qualificateur **ClassContext** a le format suivant.</span><span class="sxs-lookup"><span data-stu-id="65458-114">The **ClassContext** qualifier has the following format.</span></span>

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    <span data-ttu-id="65458-115">La valeur de keyPath peut être longue si elle comprend des clés avec des sous-clés.</span><span class="sxs-lookup"><span data-stu-id="65458-115">The value for KeyPath can be long if it includes keys with subkeys.</span></span>

    <span data-ttu-id="65458-116">L’exemple suivant montre le qualificateur **ClassContext** qui contient le chemin d’accès à un périphérique de transport d’ordinateur particulier.</span><span class="sxs-lookup"><span data-stu-id="65458-116">The following example shows the **ClassContext** qualifier that contains the path to a particular computer transport device.</span></span>

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

<span data-ttu-id="65458-117">Le modèle suivant pour une définition de classe illustre l’utilisation des qualificateurs **dynamiques**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)et **ClassContext** .</span><span class="sxs-lookup"><span data-stu-id="65458-117">The following template for a class definition illustrates the use of the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **ClassContext** qualifiers.</span></span> <span data-ttu-id="65458-118">Le fournisseur nommé par le qualificateur du **fournisseur** est le fournisseur de Registre du système d’instance.</span><span class="sxs-lookup"><span data-stu-id="65458-118">The provider named by the **Provider** qualifier is the instance System Registry provider.</span></span> <span data-ttu-id="65458-119">Sachez que les chemins de registre ne respectent pas la casse, comme les noms de qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="65458-119">Be aware that registry paths are case-insensitive, as are qualifier names.</span></span>

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

<span data-ttu-id="65458-120">Les applications de gestion peuvent également utiliser le fournisseur de Registre système pour récupérer et modifier des données de Registre pour une clé particulière.</span><span class="sxs-lookup"><span data-stu-id="65458-120">Management applications can also use the System Registry provider to retrieve and modify registry data for a particular key.</span></span>

 

 



