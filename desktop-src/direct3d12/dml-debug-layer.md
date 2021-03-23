---
title: Utilisation de la couche de débogage DirectML
description: La couche de débogage DirectML est un composant facultatif de développement qui vous permet de déboguer votre code DirectML.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104548541"
---
# <a name="using-the-directml-debug-layer"></a><span data-ttu-id="8edf0-103">Utilisation de la couche de débogage DirectML</span><span class="sxs-lookup"><span data-stu-id="8edf0-103">Using the DirectML debug layer</span></span>

<span data-ttu-id="8edf0-104">La couche de débogage DirectML est un composant facultatif de développement qui vous permet de déboguer votre code DirectML.</span><span class="sxs-lookup"><span data-stu-id="8edf0-104">The DirectML debug layer is an optional development-time component that helps you in debugging your DirectML code.</span></span> <span data-ttu-id="8edf0-105">La couche de débogage fait partie d’un package d’outils graphiques distinct, distribué en tant que [fonctionnalité à la demande](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (DOM).</span><span class="sxs-lookup"><span data-stu-id="8edf0-105">The debug layer is part of a separate Graphics Tools package, distributed as a [Feature-on-Demand](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD).</span></span> <span data-ttu-id="8edf0-106">Les DOM des outils Graphics doivent être installés sur votre système pour pouvoir utiliser la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="8edf0-106">The Graphics Tools FOD must be installed on your system in order to use the debug layer.</span></span>

<span data-ttu-id="8edf0-107">Nous vous recommandons vivement d’activer la couche de débogage lors du développement d’applications à l’aide de DirectML, car elle peut fournir des informations précieuses en cas d’utilisation d’API non valide.</span><span class="sxs-lookup"><span data-stu-id="8edf0-107">We highly recommended that you enable the debug layer while developing applications using DirectML, because it can provide invaluable information in the event of invalid API usage.</span></span>

## <a name="installing-the-directml-debug-layer"></a><span data-ttu-id="8edf0-108">Installation de la couche de débogage DirectML</span><span class="sxs-lookup"><span data-stu-id="8edf0-108">Installing the DirectML debug layer</span></span>

<span data-ttu-id="8edf0-109">Pour installer le package facultatif des outils Graphics-à la demande (DOM), exécutez la commande suivante à partir d’une invite PowerShell d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="8edf0-109">To install the optional Graphics Tools feature-on-demand (FOD) package, run the following command from an administrator Powershell prompt.</span></span>

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

<span data-ttu-id="8edf0-110">Vous pouvez également installer le package des outils Graphics à partir des paramètres de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8edf0-110">Alternatively, you can install the Graphics Tools package from within Windows 10 Settings.</span></span> <span data-ttu-id="8edf0-111">Accédez à **paramètres**  >  **applications**  >  **applications & fonctionnalités** fonctionnalités  >  **facultatives**  >  **Ajouter une fonctionnalité** > puis sélectionnez **outils graphiques**.</span><span class="sxs-lookup"><span data-stu-id="8edf0-111">Navigate to **Settings** > **Apps** > **Apps & features** > **Optional features** > **Add a feature** > then select **Graphics Tools**.</span></span>

## <a name="enabling-the-directml-debug-layer"></a><span data-ttu-id="8edf0-112">Activation de la couche de débogage DirectML</span><span class="sxs-lookup"><span data-stu-id="8edf0-112">Enabling the DirectML debug layer</span></span>

<span data-ttu-id="8edf0-113">Une fois le package d’outils Graphics installé, vous pouvez activer la couche de débogage DirectML en fournissant  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) lorsque vous appelez [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span><span class="sxs-lookup"><span data-stu-id="8edf0-113">Once the Graphics Tools package is installed, you can enable the DirectML debug layer by supplying  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) when you call [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8edf0-114">Vous devez d’abord activer la couche de débogage Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="8edf0-114">You must first enable the Direct3D 12 debug layer.</span></span> <span data-ttu-id="8edf0-115">Puis *activez la* couche de débogage DirectML en appelant **DMLCreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="8edf0-115">And *then* enable the DirectML debug layer by calling **DMLCreateDevice**.</span></span>

<span data-ttu-id="8edf0-116">Une fois que vous avez activé la couche de débogage DirectML, toutes les erreurs de DirectML ou les appels d’API non valides entraînent l’émission des informations de débogage comme sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="8edf0-116">Once you've enabled the DirectML debug layer, any DirectML errors or invalid API calls will cause debugging information to be emitted as debug output.</span></span> <span data-ttu-id="8edf0-117">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="8edf0-117">Here's an example.</span></span>

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a><span data-ttu-id="8edf0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8edf0-118">See also</span></span>

* [<span data-ttu-id="8edf0-119">DMLCreateDevice fonction)</span><span class="sxs-lookup"><span data-stu-id="8edf0-119">DMLCreateDevice function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [<span data-ttu-id="8edf0-120">Fonctionnalités disponibles-à la demande</span><span class="sxs-lookup"><span data-stu-id="8edf0-120">Available Features-on-Demand</span></span>](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [<span data-ttu-id="8edf0-121">Utiliser la validation basée sur GPU avec la couche de débogage Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8edf0-121">Use GPU-based validation with the Direct3D 12 Debug Layer</span></span>](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [<span data-ttu-id="8edf0-122">Référence de la couche de débogage Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8edf0-122">Direct3D 12 Debug Layer reference</span></span>](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
