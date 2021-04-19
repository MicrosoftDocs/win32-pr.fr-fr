---
description: Contient les attributs de partage DDE gérés par le gestionnaire de base de données du partage NetDDE (DSDM).
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: NDDESHAREINFO, structure (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545077"
---
# <a name="nddeshareinfo-structure"></a><span data-ttu-id="3add4-103">NDDESHAREINFO, structure</span><span class="sxs-lookup"><span data-stu-id="3add4-103">NDDESHAREINFO structure</span></span>

<span data-ttu-id="3add4-104">\[Le DDE réseau n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3add4-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="3add4-105">Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]</span><span class="sxs-lookup"><span data-stu-id="3add4-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="3add4-106">Contient les attributs de partage DDE gérés par le gestionnaire de base de données du partage NetDDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="3add4-106">Contains DDE share attributes maintained by the NetDDE Share Database Manager (DSDM).</span></span> <span data-ttu-id="3add4-107">Le descripteur de sécurité associé à chaque partage DDE n’est pas transmis via cette structure, mais est accessible via des fonctions spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3add4-107">The security descriptor associated with each DDE share is not passed through this structure but is accessed through specific functions.</span></span> <span data-ttu-id="3add4-108">L’API DSDM NetDDE accepte cette structure pour les fonctions set. pour les fonctions d’extraction, le DSDM retourne la structure compressée dans la mémoire tampon fournie avec les données référencées par les membres **lpszShareName**, **lpszAppTopicList** et **lpszItemList**.</span><span class="sxs-lookup"><span data-stu-id="3add4-108">The NetDDE DSDM API accepts this structure for set functions; for get functions, the DSDM returns the structure packed into the supplied buffer along with the data referenced by the members **lpszShareName**, **lpszAppTopicList**, and **lpszItemList**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3add4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3add4-109">Syntax</span></span>


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a><span data-ttu-id="3add4-110">Membres</span><span class="sxs-lookup"><span data-stu-id="3add4-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="3add4-111">**lRevision**</span><span class="sxs-lookup"><span data-stu-id="3add4-111">**lRevision**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-112">Niveau de révision de la structure **NDDESHAREINFO** .</span><span class="sxs-lookup"><span data-stu-id="3add4-112">The revision level of the **NDDESHAREINFO** structure.</span></span> <span data-ttu-id="3add4-113">Actuellement, le niveau de révision est 1.</span><span class="sxs-lookup"><span data-stu-id="3add4-113">Currently, the revision level is 1.</span></span>

</dd> <dt>

<span data-ttu-id="3add4-114">**lpszShareName**</span><span class="sxs-lookup"><span data-stu-id="3add4-114">**lpszShareName**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-115">Nom du partage.</span><span class="sxs-lookup"><span data-stu-id="3add4-115">The name of the share.</span></span> <span data-ttu-id="3add4-116">Cette chaîne ne doit pas être supérieure à la longueur maximale de \_ NDDESHARENAME caractères.</span><span class="sxs-lookup"><span data-stu-id="3add4-116">This string must be no more than MAX\_NDDESHARENAME characters long.</span></span>

</dd> <dt>

<span data-ttu-id="3add4-117">**lShareType**</span><span class="sxs-lookup"><span data-stu-id="3add4-117">**lShareType**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-118">Un ou plusieurs types de partage DDE.</span><span class="sxs-lookup"><span data-stu-id="3add4-118">One or more DDE share types.</span></span> <span data-ttu-id="3add4-119">Ce membre peut être une combinaison des types de partage DDE pris en charge suivants.</span><span class="sxs-lookup"><span data-stu-id="3add4-119">This member can be a combination of the following supported DDE share types.</span></span>



| <span data-ttu-id="3add4-120">Type de partage</span><span class="sxs-lookup"><span data-stu-id="3add4-120">Share type</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="3add4-121">Signification</span><span class="sxs-lookup"><span data-stu-id="3add4-121">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <span data-ttu-id="3add4-122"><dt>**Partager \_ TAPEZ \_ New**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="3add4-122"><dt>**SHARE\_TYPE\_NEW**</dt> <dt>0x02</dt></span></span> </dl>          | <span data-ttu-id="3add4-123">Le partage contient une paire application/rubrique OLE.</span><span class="sxs-lookup"><span data-stu-id="3add4-123">The share contains an OLE application/topic pair.</span></span><br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <span data-ttu-id="3add4-124"><dt>**Partager \_ TAPEZ \_ Old**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="3add4-124"><dt>**SHARE\_TYPE\_OLD**</dt> <dt>0x01</dt></span></span> </dl>          | <span data-ttu-id="3add4-125">Le partage contient une paire application/rubrique DDE.</span><span class="sxs-lookup"><span data-stu-id="3add4-125">The share contains a DDE application/topic pair.</span></span><br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <span data-ttu-id="3add4-126"><dt>**Partager \_ 0x04 \_ statique de type**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3add4-126"><dt>**SHARE\_TYPE\_STATIC**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="3add4-127">Le partage contient une paire application/rubrique statique.</span><span class="sxs-lookup"><span data-stu-id="3add4-127">The share contains a static application/topic pair.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3add4-128">**lpszAppTopicList**</span><span class="sxs-lookup"><span data-stu-id="3add4-128">**lpszAppTopicList**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-129">Pointeur vers une mémoire tampon qui contient des chaînes se terminant par un caractère null pour les paires d’application/rubrique statiques DDE, OLE et.</span><span class="sxs-lookup"><span data-stu-id="3add4-129">A pointer to a buffer containing null-terminated strings for the DDE, OLE, and static application/topic pairs.</span></span> <span data-ttu-id="3add4-130">La mémoire tampon doit être au format suivant :</span><span class="sxs-lookup"><span data-stu-id="3add4-130">The buffer should be in the following format:</span></span>

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

<span data-ttu-id="3add4-131">**fSharedFlag**</span><span class="sxs-lookup"><span data-stu-id="3add4-131">**fSharedFlag**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-132">Si ce membre a la **valeur false**, le partage DDE n’autorise pas les utilisateurs distants à communiquer via ce dernier à l’aide de DDE.</span><span class="sxs-lookup"><span data-stu-id="3add4-132">If this member is **FALSE**, the DDE share will not allow remote users to communicate through it by using DDE.</span></span> <span data-ttu-id="3add4-133">Toutefois, les utilisateurs locaux peuvent toujours communiquer via le partage DDE.</span><span class="sxs-lookup"><span data-stu-id="3add4-133">However, local users can still communicate through the DDE share.</span></span> <span data-ttu-id="3add4-134">Les liens client locaux sont toujours implicites si le DACL associé accorde l’accès.</span><span class="sxs-lookup"><span data-stu-id="3add4-134">Local client links are always implied if the associated DACL grants access.</span></span>

</dd> <dt>

<span data-ttu-id="3add4-135">**fService**</span><span class="sxs-lookup"><span data-stu-id="3add4-135">**fService**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-136">Si ce membre est défini, le partage DDE ne vérifie pas si l’utilisateur actuel l’a défini comme approuvé avant d’autoriser la communication DDE.</span><span class="sxs-lookup"><span data-stu-id="3add4-136">If this member is set, the DDE share will not check whether the current user has set it as trusted before allowing DDE communication.</span></span>

</dd> <dt>

<span data-ttu-id="3add4-137">**fStartAppFlag**</span><span class="sxs-lookup"><span data-stu-id="3add4-137">**fStartAppFlag**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-138">Si ce membre est défini et que le partage est approuvé pour démarrer des applications, NetDDE tente de démarrer l’application spécifiée par **lpszAppTopicList** s’il ne peut pas démarrer une conversation DDE avec l’application.</span><span class="sxs-lookup"><span data-stu-id="3add4-138">If this member is set and the share is trusted to start applications, NetDDE will attempt to start the application specified by **lpszAppTopicList** if it cannot initially start a DDE conversation with the application.</span></span>

</dd> <dt>

<span data-ttu-id="3add4-139">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="3add4-139">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-140">Lorsque NetDDE démarre une application pour initier une conversation DDE, cette valeur est envoyée à l’application via le paramètre *nCmdShow* de la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="3add4-140">When NetDDE starts an application to initiate a DDE conversation, this value is sent to the application through the *nCmdShow* parameter of the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="3add4-141">Il définit le mode par défaut de la fenêtre d’application à afficher dans.</span><span class="sxs-lookup"><span data-stu-id="3add4-141">It defines the preferred mode for the application window to be shown in.</span></span> <span data-ttu-id="3add4-142">Ce paramètre est significatif uniquement si **fStartAppFlag** est actif.</span><span class="sxs-lookup"><span data-stu-id="3add4-142">This parameter is significant only if **fStartAppFlag** is active.</span></span> <span data-ttu-id="3add4-143">L’utilisateur connecté dans le contexte duquel l’application est démarrée peut également remplacer cette option lors de la promotion de l’état de confiance du partage.</span><span class="sxs-lookup"><span data-stu-id="3add4-143">The logged on user in whose context the application is started can also override this option when promoting the share to trusted status.</span></span> <span data-ttu-id="3add4-144">La valeur par défaut de ce membre est SW \_ SHOWMAXIMIZED.</span><span class="sxs-lookup"><span data-stu-id="3add4-144">The default for this member is SW\_SHOWMAXIMIZED.</span></span>

</dd> <dt>

<span data-ttu-id="3add4-145">**qModifyId**</span><span class="sxs-lookup"><span data-stu-id="3add4-145">**qModifyId**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-146">Numéro de série de 8 octets qui indique le numéro de série de modification du partage DDE.</span><span class="sxs-lookup"><span data-stu-id="3add4-146">An 8-byte serial number that indicates the modification serial number of the DDE share.</span></span> <span data-ttu-id="3add4-147">Chaque fois que le partage DDE est modifié par un appel [**NDdeShareSetInfo**](nddesharesetinfo.md) ou [**NDdeSetShareSecurity**](nddesetsharesecurity.md) , ces valeurs sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="3add4-147">Every time the DDE share is modified by a [**NDdeShareSetInfo**](nddesharesetinfo.md) or [**NDdeSetShareSecurity**](nddesetsharesecurity.md) call, these values are changed.</span></span>

</dd> <dt>

<span data-ttu-id="3add4-148">**cNumItems**</span><span class="sxs-lookup"><span data-stu-id="3add4-148">**cNumItems**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-149">Nombre d’éléments figurant dans **lpszItemList**.</span><span class="sxs-lookup"><span data-stu-id="3add4-149">The number of items listed in **lpszItemList**.</span></span> <span data-ttu-id="3add4-150">Si **cNumItems** est égal à zéro, **lpszItemList** est vide, et les informations de partage et le descripteur de sécurité associé s’appliquent à tous les éléments qui ont été mis en service par l’application associée.</span><span class="sxs-lookup"><span data-stu-id="3add4-150">If **cNumItems** is zero, then **lpszItemList** is empty, and the share information and associated security descriptor apply to all items serviced by the associated application.</span></span>

</dd> <dt>

<span data-ttu-id="3add4-151">**lpszItemList**</span><span class="sxs-lookup"><span data-stu-id="3add4-151">**lpszItemList**</span></span>
</dt> <dd>

<span data-ttu-id="3add4-152">Pointeur vers une mémoire tampon qui contient des chaînes se terminant par un caractère null qui spécifient les éléments que l’application cliente dans une transaction DDE peut demander ou pour démarrer des boucles de notification.</span><span class="sxs-lookup"><span data-stu-id="3add4-152">A pointer to a buffer containing null-terminated strings that specify the items the client application in a DDE transaction can request or start advise loops on.</span></span> <span data-ttu-id="3add4-153">Si aucun élément n’est répertorié, le partage DDE autorise l’utilisation de tout élément.</span><span class="sxs-lookup"><span data-stu-id="3add4-153">If no items are listed, the DDE share allows any item to be used.</span></span> <span data-ttu-id="3add4-154">Le nombre d’éléments dans la liste doit correspondre au nombre de **cNumItems** .</span><span class="sxs-lookup"><span data-stu-id="3add4-154">The number of items in the list must match the **cNumItems** count.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3add4-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3add4-155">Requirements</span></span>



| <span data-ttu-id="3add4-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3add4-156">Requirement</span></span> | <span data-ttu-id="3add4-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="3add4-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3add4-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3add4-158">Minimum supported client</span></span><br/> | <span data-ttu-id="3add4-159">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3add4-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3add4-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3add4-160">Minimum supported server</span></span><br/> | <span data-ttu-id="3add4-161">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3add4-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3add4-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="3add4-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="3add4-163"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3add4-163"><dt>Nddeapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3add4-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3add4-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3add4-165">Présentation du échange dynamique de données réseau</span><span class="sxs-lookup"><span data-stu-id="3add4-165">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="3add4-166">Structures DDE réseau</span><span class="sxs-lookup"><span data-stu-id="3add4-166">Network DDE Structures</span></span>](network-dde-structures.md)
</dt> <dt>

[<span data-ttu-id="3add4-167">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="3add4-167">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> <dt>

[<span data-ttu-id="3add4-168">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="3add4-168">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> <dt>

[<span data-ttu-id="3add4-169">**WinMain**</span><span class="sxs-lookup"><span data-stu-id="3add4-169">**WinMain**</span></span>](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

