---
title: Insertable (clé CLSID)
description: Indique que les objets de cette classe doivent apparaître dans la zone de liste de la boîte de dialogue Insérer un objet lorsqu’ils sont utilisés par les applications de conteneur COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- Clé de Registre Insertable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032246"
---
# <a name="insertable-clsid-key"></a><span data-ttu-id="4c0aa-104">Insertable (clé CLSID)</span><span class="sxs-lookup"><span data-stu-id="4c0aa-104">Insertable (CLSID Key)</span></span>

<span data-ttu-id="4c0aa-105">Indique que les objets de cette classe doivent apparaître dans la zone de liste de la boîte de dialogue **Insérer un objet** lorsqu’ils sont utilisés par les applications de conteneur com.</span><span class="sxs-lookup"><span data-stu-id="4c0aa-105">Indicates that objects of this class should appear in the **Insert Object** dialog box list box when used by COM container applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4c0aa-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="4c0aa-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a><span data-ttu-id="4c0aa-107">Notes</span><span class="sxs-lookup"><span data-stu-id="4c0aa-107">Remarks</span></span>

<span data-ttu-id="4c0aa-108">Cette clé est une entrée obligatoire pour les applications COM 32 bits dont les objets peuvent être insérés dans des applications 16 bits existantes.</span><span class="sxs-lookup"><span data-stu-id="4c0aa-108">This key is a required entry for 32-bit COM applications whose objects can be inserted into existing 16-bit applications.</span></span> <span data-ttu-id="4c0aa-109">Les applications 16 bits existantes recherchent dans le registre cette clé, qui informe l’application que le serveur prend en charge les incorporations.</span><span class="sxs-lookup"><span data-stu-id="4c0aa-109">Existing 16-bit applications look in the registry for this key, which informs the application that the server supports embeddings.</span></span> <span data-ttu-id="4c0aa-110">Si la clé pouvant être **insérée** existe, les applications 16 bits peuvent également essayer de vérifier que le serveur existe sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4c0aa-110">If the **Insertable** key exists, 16-bit applications may also attempt to verify that the server exists on the machine.</span></span> <span data-ttu-id="4c0aa-111">les applications 16 bits récupèrent généralement la valeur de la clé [**LocalServer**](localserver.md) de la classe et vérifient s’il s’agit d’un fichier valide sur le système.</span><span class="sxs-lookup"><span data-stu-id="4c0aa-111">16-bit applications typically retrieve the value of the [**LocalServer**](localserver.md) key from the class and check to see whether it is a valid file on the system.</span></span> <span data-ttu-id="4c0aa-112">Par conséquent, pour qu’une application 32 bits soit à pouvoir être insérée par une application 16 bits, l’application 32 bits doit inscrire la sous-clé **LocalServer** en plus de l’inscription [**LocalServer32**](localserver32.md).</span><span class="sxs-lookup"><span data-stu-id="4c0aa-112">Therefore, for a 32-bit application to be insertable by a 16-bit application, the 32-bit application should register the **LocalServer** subkey in addition to registering [**LocalServer32**](localserver32.md).</span></span>

<span data-ttu-id="4c0aa-113">Utilisé avec les contrôles, cette entrée indique qu’un objet peut agir uniquement comme un objet incorporé sur place sans fonctionnalités de contrôle spéciales.</span><span class="sxs-lookup"><span data-stu-id="4c0aa-113">Used with controls, this entry indicates that an object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="4c0aa-114">Les objets qui ont cette clé s’affichent dans la boîte de dialogue **Insérer un objet** pour leur conteneur.</span><span class="sxs-lookup"><span data-stu-id="4c0aa-114">Objects that have this key appear in the **Insert Object** dialog box for their container.</span></span> <span data-ttu-id="4c0aa-115">Lorsqu’elle est utilisée avec les contrôles, cette entrée indique également que le contrôle a été testé avec des conteneurs sans contrôle.</span><span class="sxs-lookup"><span data-stu-id="4c0aa-115">When used with controls, this entry also indicates the control has been tested with non-control containers.</span></span> <span data-ttu-id="4c0aa-116">Cette entrée est également facultative et peut être omise lorsqu’un contrôle n’est pas conçu pour fonctionner avec des conteneurs plus anciens qui ne comprennent pas de contrôles.</span><span class="sxs-lookup"><span data-stu-id="4c0aa-116">This entry is also optional and can be omitted when a control is not designed to work with older containers that do not understand controls.</span></span>

> [!Note]  
> <span data-ttu-id="4c0aa-117">Cette clé n’est pas présente pour les classes internes comme les classes moniker.</span><span class="sxs-lookup"><span data-stu-id="4c0aa-117">This key is not present for internal classes like the moniker classes.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4c0aa-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c0aa-118">Related topics</span></span>

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




