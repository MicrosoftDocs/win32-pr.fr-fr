---
title: Structures de plug-in
description: Structures pour le développement d’applications clientes par l’API Windows Biometric Framework.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- API Windows Biometric Framework API Windows Biometric Framework, structures de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310877"
---
# <a name="plug-in-structures"></a><span data-ttu-id="b1afb-104">Structures de plug-in</span><span class="sxs-lookup"><span data-stu-id="b1afb-104">Plug-in Structures</span></span>

<span data-ttu-id="b1afb-105">Les structures suivantes sont prises en charge pour le développement d’applications clientes par l’API Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="b1afb-105">The following structures are supported for client application development by the Windows Biometric Framework API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b1afb-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b1afb-106">In this section</span></span>



| <span data-ttu-id="b1afb-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b1afb-107">Topic</span></span>                                                                                                | <span data-ttu-id="b1afb-108">Description</span><span class="sxs-lookup"><span data-stu-id="b1afb-108">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1afb-109">**\_stratégie de compte WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="b1afb-109">**WINBIO\_ACCOUNT\_POLICY**</span></span>](winbio-account-policy.md)<br/>                                  | <span data-ttu-id="b1afb-110">Contient une stratégie d’antiusurpation propre à la valeur par défaut ou spécifique au compte.</span><span class="sxs-lookup"><span data-stu-id="b1afb-110">Contains either a default or account-specific antispoofing policy.</span></span><br/>                                                         |
| [<span data-ttu-id="b1afb-111">**VERSION de l’interface de l' \_ adaptateur WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b1afb-111">**WINBIO\_ADAPTER\_INTERFACE\_VERSION**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | <span data-ttu-id="b1afb-112">Contient un numéro de version majeure et mineure utilisé dans les tables du moteur, du capteur et de l’interface de l’adaptateur de stockage.</span><span class="sxs-lookup"><span data-stu-id="b1afb-112">Contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.</span></span><br/>                |
| [<span data-ttu-id="b1afb-113">**\_interface du moteur WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="b1afb-113">**WINBIO\_ENGINE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | <span data-ttu-id="b1afb-114">Contient des pointeurs vers vos fonctions d’adaptateur de moteur personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b1afb-114">Contains pointers to your custom engine adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="b1afb-115">**\_paramètres d' \_ inscription étendue WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="b1afb-115">**WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS**</span></span>](winbio-extended-enrollment-parameters.md)<br/> | <span data-ttu-id="b1afb-116">Contient des informations supplémentaires nécessaires à un adaptateur de moteur pour créer un modèle d’inscription.</span><span class="sxs-lookup"><span data-stu-id="b1afb-116">Contains additional information that an engine adapter needs to create an enrollment template.</span></span> <br/>                            |
| [<span data-ttu-id="b1afb-117">**\_pipeline WINBIO**</span><span class="sxs-lookup"><span data-stu-id="b1afb-117">**WINBIO\_PIPELINE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | <span data-ttu-id="b1afb-118">Contient les informations de contexte partagé utilisées par les composants de capteur, de moteur et d’adaptateur de stockage dans une seule unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="b1afb-118">Contains shared context information used by the sensor, engine, and storage adapter components in a single biometric unit.</span></span><br/> |
| [<span data-ttu-id="b1afb-119">**\_interface du capteur WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="b1afb-119">**WINBIO\_SENSOR\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | <span data-ttu-id="b1afb-120">Contient des pointeurs vers vos fonctions d’adaptateur de capteur personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b1afb-120">Contains pointers to your custom sensor adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="b1afb-121">**\_interface de stockage WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="b1afb-121">**WINBIO\_STORAGE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | <span data-ttu-id="b1afb-122">Contient des pointeurs vers vos fonctions d’adaptateur de stockage personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b1afb-122">Contains pointers to your custom storage adapter functions.</span></span><br/>                                                                |
| [<span data-ttu-id="b1afb-123">**\_enregistrement de stockage WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="b1afb-123">**WINBIO\_STORAGE\_RECORD**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | <span data-ttu-id="b1afb-124">Contient un modèle biométrique et les données associées dans un format standard.</span><span class="sxs-lookup"><span data-stu-id="b1afb-124">Contains a biometric template and associated data in a standard format.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="b1afb-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1afb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1afb-126">Référence du plug-in</span><span class="sxs-lookup"><span data-stu-id="b1afb-126">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> <dt>

[<span data-ttu-id="b1afb-127">Fonctions de plug-in</span><span class="sxs-lookup"><span data-stu-id="b1afb-127">Plug-in Functions</span></span>](plug-in-functions.md)
</dt> <dt>

[<span data-ttu-id="b1afb-128">**WbioQueryEngineInterface**</span><span class="sxs-lookup"><span data-stu-id="b1afb-128">**WbioQueryEngineInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[<span data-ttu-id="b1afb-129">**WbioQuerySensorInterface**</span><span class="sxs-lookup"><span data-stu-id="b1afb-129">**WbioQuerySensorInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[<span data-ttu-id="b1afb-130">**WbioQueryStorageInterface**</span><span class="sxs-lookup"><span data-stu-id="b1afb-130">**WbioQueryStorageInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





