---
description: Le modèle COM (Component Object Model) est une norme binaire pour l’écriture de logiciels de composants dans un environnement informatique distribué.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Sauvegarde et restauration de la base de données d’inscription de classe COM+ sous VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526967"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a><span data-ttu-id="8719f-103">Sauvegarde et restauration de la base de données d’inscription de classe COM+ sous VSS</span><span class="sxs-lookup"><span data-stu-id="8719f-103">Backing Up and Restoring the COM+ Class Registration Database Under VSS</span></span>

<span data-ttu-id="8719f-104">Le modèle COM (Component Object Model) est une norme binaire pour l’écriture de logiciels de composants dans un environnement informatique distribué.</span><span class="sxs-lookup"><span data-stu-id="8719f-104">The Component Object Model (COM) is a binary standard for writing component software in a distributed computing environment.</span></span>

<span data-ttu-id="8719f-105">Identificateurs de composant (GUID) d’implémentation Win32 d’origine et autre État COM dans le Registre sous **le \_ \_ \\ CLSID racine des classes HKEY**.</span><span class="sxs-lookup"><span data-stu-id="8719f-105">The original Win32 implementation stored component identifiers (GUIDs) and other COM state in the registry under **HKEY\_CLASSES\_ROOT\\CLSID**.</span></span>

<span data-ttu-id="8719f-106">La génération actuelle du modèle COM (Component Object Model), COM+, offre une base de données indépendante du Registre pour le stockage des informations d’inscription du composant : la base de données d’inscription de classe COM+.</span><span class="sxs-lookup"><span data-stu-id="8719f-106">The current generation of the Component Object Model, COM+, offers a registry-independent database for storing component registration information: the COM+ Class Registration Database.</span></span>

<span data-ttu-id="8719f-107">La base de données d’inscription de classe COM+ prend en charge un enregistreur VSS, qui permet aux demandeurs de sauvegarder la base de données d’inscription à l’aide des données stockées sur un volume copié par cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="8719f-107">The COM+ Class Registration Database supports a VSS writer, which allows requesters to back up the registration database using data stored on a shadow-copied volume.</span></span>

<span data-ttu-id="8719f-108">Pour restaurer la base de données d’inscription COM+, un demandeur doit appeler la méthode [ICOMAdminCatalog :: RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .</span><span class="sxs-lookup"><span data-stu-id="8719f-108">To restore the COM+ Registration Database, a requester must call the [ICOMAdminCatalog::RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="8719f-109">Pour plus d’informations sur le writer de base de données d’inscription COM+, consultez la page [enregistreurs VSS](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="8719f-109">For more information about the COM+ Registration Database writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
