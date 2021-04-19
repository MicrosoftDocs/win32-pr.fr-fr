---
title: Fonctions des extensions NPS
description: Fonctions des extensions NPS
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510271"
---
# <a name="nps-extensions-functions"></a>Fonctions des extensions NPS

> [!Note]  
> Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

## <a name="application-defined"></a>Application définie

L’architecture des dll d’extension NPS prend en charge les fonctions exportées suivantes :

-   [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

Les fonctions [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) et [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) sont facultatives.

La DLL d’extension peut exporter [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) au lieu de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) ou [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).

Si la DLL d’extension exporte [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), elle doit également exporter [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).

## <a name="system-defined"></a>Défini par le système

Lorsque NPS appelle une implémentation de [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS transmet à la fonction un pointeur vers une structure de [**\_ bloc de \_ contrôle \_ d’extension RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .

La structure de [**\_ bloc de \_ contrôle \_ d’extension RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contient des pointeurs de fonction vers les fonctions suivantes fournies par NPS :

-   [**GetRequest**](/previous-versions/ms688263(v=vs.85))
-   [**GetResponse**](/previous-versions/ms688270(v=vs.85))
-   [**SetResponseType**](/previous-versions/ms688462(v=vs.85))

Les fonctions [**GetRequest**](/previous-versions/ms688263(v=vs.85)) et [**GetResponse**](/previous-versions/ms688270(v=vs.85)) retournent des pointeurs vers une structure de type [**\_ \_ tableau d’attributs RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).

La structure du [**\_ \_ tableau d’attributs RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contient des pointeurs de fonction vers les fonctions suivantes fournies par NPS :

-   [**Complémentaires**](/previous-versions/ms688246(v=vs.85))
-   [**AttributeAt**](/previous-versions/ms688253(v=vs.85))
-   [**GetSize,**](/previous-versions/ms688277(v=vs.85))
-   [**InsertAt**](/previous-versions/ms688296(v=vs.85))
-   [**RemoveAt**](/previous-versions/ms688452(v=vs.85))
-   [**SetAt**](/previous-versions/ms688456(v=vs.85))

 

 