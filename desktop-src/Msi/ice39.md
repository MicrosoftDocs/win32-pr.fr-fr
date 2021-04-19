---
description: ICE39 valide le flux d’informations de synthèse de la base de données.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523279"
---
# <a name="ice39"></a><span data-ttu-id="919ab-103">ICE39</span><span class="sxs-lookup"><span data-stu-id="919ab-103">ICE39</span></span>

<span data-ttu-id="919ab-104">ICE39 valide le [flux d’informations de synthèse](summary-information-stream.md) de la base de données.</span><span class="sxs-lookup"><span data-stu-id="919ab-104">ICE39 validates the [Summary Information Stream](summary-information-stream.md) of the database.</span></span>

<span data-ttu-id="919ab-105">ICE39 vérifie le format des propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="919ab-105">ICE39 checks the format of the following properties:</span></span>

-   [<span data-ttu-id="919ab-106">**Résumé du nombre de mots**</span><span class="sxs-lookup"><span data-stu-id="919ab-106">**Word Count Summary**</span></span>](word-count-summary.md)
-   [<span data-ttu-id="919ab-107">**Résumé du nombre de pages**</span><span class="sxs-lookup"><span data-stu-id="919ab-107">**Page Count Summary**</span></span>](page-count-summary.md)
-   [<span data-ttu-id="919ab-108">**Résumé du modèle**</span><span class="sxs-lookup"><span data-stu-id="919ab-108">**Template Summary**</span></span>](template-summary.md)
-   [<span data-ttu-id="919ab-109">**Résumé du numéro de révision**</span><span class="sxs-lookup"><span data-stu-id="919ab-109">**Revision Number Summary**</span></span>](revision-number-summary.md)
-   [<span data-ttu-id="919ab-110">**Créer un résumé de l’heure/date**</span><span class="sxs-lookup"><span data-stu-id="919ab-110">**Create Time/Date Summary**</span></span>](create-time-date-summary.md)
-   [<span data-ttu-id="919ab-111">**Résumé de l’heure/date du dernier enregistrement**</span><span class="sxs-lookup"><span data-stu-id="919ab-111">**Last Saved Time/Date Summary**</span></span>](last-saved-time-date-summary.md)
-   [<span data-ttu-id="919ab-112">**Dernier Résumé imprimé**</span><span class="sxs-lookup"><span data-stu-id="919ab-112">**Last Printed Summary**</span></span>](last-printed-summary.md)

<span data-ttu-id="919ab-113">Si la propriété [**Résumé du nombre de mots**](word-count-summary.md) spécifie que la source est compressée, ICE39 publie un avertissement si des fichiers sont également marqués comme compressés dans la colonne attributs de la table de [fichiers](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="919ab-113">If the [**Word Count Summary**](word-count-summary.md) Property specifies that the source is compressed, ICE39 posts a warning if any files are also marked as compressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="919ab-114">Consultez [utilisation des armoires et des sources compressées](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="919ab-114">See [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="919ab-115">ICE39 publie un avertissement si la propriété [**Résumé du nombre de mots**](word-count-summary.md) spécifie que le package est conforme au contrôle de compte d’utilisateur et que la [table MsiPackageCertificate](msipackagecertificate-table.md) n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="919ab-115">ICE39 posts a warning if the [**Word Count Summary**](word-count-summary.md) Property specifies that the package is UAC compliant and the [MsiPackageCertificate Table](msipackagecertificate-table.md) is not empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="919ab-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="919ab-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="919ab-117">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="919ab-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



