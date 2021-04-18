---
description: Obtient les données brutes pour une structure E-EDID (Enhanced Display standard Association) améliorée de la norme VESA (Video Electronics Association) qui définit des paramètres optimaux pour la configuration d’une analyse.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: Méthode WmiGetMonitorRawEEdidV1Block de la classe WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533674"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a><span data-ttu-id="46cad-103">Méthode WmiGetMonitorRawEEdidV1Block de la classe WmiMonitorDescriptorMethods</span><span class="sxs-lookup"><span data-stu-id="46cad-103">WmiGetMonitorRawEEdidV1Block method of the WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="46cad-104">La méthode **WmiGetMonitorRawEEdidV1Block** obtient les données brutes pour une structure de données d’identification d’affichage étendu (E-EDID) améliorée d’association Video Electronics standard Association (VESA) qui définit des paramètres optimaux pour la configuration d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="46cad-104">The **WmiGetMonitorRawEEdidV1Block** method gets the raw data for a specified Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure that defines optimal settings for configuring a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="46cad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46cad-105">Syntax</span></span>


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a><span data-ttu-id="46cad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46cad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46cad-107">*BlockId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46cad-107">*BlockId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46cad-108">Identité du bloc de données.</span><span class="sxs-lookup"><span data-stu-id="46cad-108">The data block identity.</span></span>

</dd> <dt>

<span data-ttu-id="46cad-109">*BlockType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46cad-109">*BlockType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46cad-110">Type de bloc de données.</span><span class="sxs-lookup"><span data-stu-id="46cad-110">Type of data block.</span></span> <span data-ttu-id="46cad-111">Le tableau suivant répertorie les valeurs de retour possibles.</span><span class="sxs-lookup"><span data-stu-id="46cad-111">The following table lists possible return values.</span></span>



| <span data-ttu-id="46cad-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="46cad-112">Value</span></span>                                                                                 | <span data-ttu-id="46cad-113">Signification</span><span class="sxs-lookup"><span data-stu-id="46cad-113">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="46cad-114"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="46cad-114"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="46cad-115">Non initialisé(e)</span><span class="sxs-lookup"><span data-stu-id="46cad-115">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="46cad-116"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="46cad-116"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="46cad-117">Bloc de base EDID</span><span class="sxs-lookup"><span data-stu-id="46cad-117">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="46cad-118"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="46cad-118"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="46cad-119">Carte de blocs EDID</span><span class="sxs-lookup"><span data-stu-id="46cad-119">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="46cad-120"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="46cad-120"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="46cad-121">Autres</span><span class="sxs-lookup"><span data-stu-id="46cad-121">Other</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="46cad-122">*BlockContent* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46cad-122">*BlockContent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46cad-123">Tableau de 128 octets qui contient le contenu du bloc brut.</span><span class="sxs-lookup"><span data-stu-id="46cad-123">A 128-byte array that contains the raw block content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46cad-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46cad-124">Return value</span></span>

<span data-ttu-id="46cad-125">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="46cad-125">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="46cad-126">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="46cad-126">Any other number indicates an error.</span></span> <span data-ttu-id="46cad-127">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="46cad-127">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="46cad-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="46cad-128">Examples</span></span>

<span data-ttu-id="46cad-129">L’exemple de code suivant récupère les blocs EDID de n’importe quel affichage sous la forme de tableaux 128 bits bruts.</span><span class="sxs-lookup"><span data-stu-id="46cad-129">The following code example retrieves the EDID blocks of any display as raw 128 bit arrays.</span></span>


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="46cad-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46cad-130">Requirements</span></span>



| <span data-ttu-id="46cad-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46cad-131">Requirement</span></span> | <span data-ttu-id="46cad-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="46cad-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46cad-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46cad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="46cad-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46cad-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="46cad-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46cad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="46cad-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46cad-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="46cad-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="46cad-137">Namespace</span></span><br/>                | <span data-ttu-id="46cad-138">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="46cad-138">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="46cad-139">MOF</span><span class="sxs-lookup"><span data-stu-id="46cad-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46cad-140"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46cad-140"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="46cad-141">DLL</span><span class="sxs-lookup"><span data-stu-id="46cad-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46cad-142"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46cad-142"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46cad-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46cad-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46cad-144">**WmiMonitorDescriptorMethods**</span><span class="sxs-lookup"><span data-stu-id="46cad-144">**WmiMonitorDescriptorMethods**</span></span>](wmimonitordescriptormethods.md)
</dt> <dt>

[<span data-ttu-id="46cad-145">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="46cad-145">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

