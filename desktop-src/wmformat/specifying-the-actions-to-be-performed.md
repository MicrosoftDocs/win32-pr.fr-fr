---
title: Spécification des actions à effectuer
description: Spécification des actions à effectuer
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- ASF (Advanced Systems Format), spécification des actions
- ASF (format des systèmes avancés), spécification des actions
- gestion des droits numériques (DRM), spécification des actions
- DRM (gestion des droits numériques), spécification des actions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2bd39a04d9ac87c4492749ca5e250d587c0e25
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381539"
---
# <a name="specifying-the-actions-to-be-performed"></a><span data-ttu-id="f2770-107">Spécification des actions à effectuer</span><span class="sxs-lookup"><span data-stu-id="f2770-107">Specifying the Actions To Be Performed</span></span>

<span data-ttu-id="f2770-108">Quand vous appelez [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) pour la première fois pour créer l’objet lecteur, le deuxième paramètre est **un opérateur de bits or de** valeurs de [**\_ droits WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .</span><span class="sxs-lookup"><span data-stu-id="f2770-108">When you first call [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) to create the reader object, the second parameter is a bitwise **OR** of [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) values.</span></span> <span data-ttu-id="f2770-109">Utilisez ce paramètre pour spécifier la ou les actions que l’application doit effectuer sur le premier fichier à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f2770-109">Use this parameter to specify which action(s) the application will take on the first file to be opened.</span></span> <span data-ttu-id="f2770-110">Ces actions correspondent directement aux droits qui peuvent être spécifiés dans la licence.</span><span class="sxs-lookup"><span data-stu-id="f2770-110">These actions correspond directly to rights that can be specified in the license.</span></span> <span data-ttu-id="f2770-111">Lors des appels suivants à [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), vous pouvez modifier les droits que vous demandez en appelant [**IWMDRMReader :: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), en spécifiant la constante définie pour la propriété des [**\_ droits DRM**](drm-rights.md) et en utilisant des littéraux de chaîne (de type **WCHAR**) séparés par des points-virgules pour identifier les droits.</span><span class="sxs-lookup"><span data-stu-id="f2770-111">On subsequent calls to [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can modify the rights that you are requesting by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), specifying the defined constant for the [**DRM\_Rights**](drm-rights.md) property, and using string literals (of type **WCHAR**) separated by semicolons to identify the rights.</span></span> <span data-ttu-id="f2770-112">L’extrait de code suivant demande quatre droits : lire le fichier, le copier sur un appareil et le lire dans le cadre d’une sélection collaborative.</span><span class="sxs-lookup"><span data-stu-id="f2770-112">The following code snippet requests four rights: play the file, copy it to a device, and play it as part of a collaborative playlist.</span></span>


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> <span data-ttu-id="f2770-113">Ne confondez pas la propriété [**\_ droits DRM**](drm-rights.md) avec la propriété [**\_ indicateurs DRM**](drm-flags.md) , qui est un **DWORD** utilisé pour spécifier les droits à appliquer à une licence locale DRM version 1 lors de la copie du contenu à partir d’un CD.</span><span class="sxs-lookup"><span data-stu-id="f2770-113">Do not confuse the [**DRM\_Rights**](drm-rights.md) property with the [**DRM\_Flags**](drm-flags.md) property, which is a **DWORD** used to specify which rights to apply to a local DRM version 1 license when copying content from a CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f2770-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f2770-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2770-115">**Lecture des fichiers protégés**</span><span class="sxs-lookup"><span data-stu-id="f2770-115">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




