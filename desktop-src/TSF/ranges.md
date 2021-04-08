---
title: Plages
description: Plages
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- Text Services Framework (TSF), plages
- TSF (Text Services Framework), plages
- services de texte, plages
- Applications compatibles TSF, plages
- ranges
- Text Services Framework (TSF), ancres
- TSF (Text Services Framework), ancres
- services de texte, ancres
- Applications compatibles TSF, ancres
- Points d’ancrage
- Text Services Framework (TSF), clones
- TSF (Text Services Framework), clones
- services de texte, clones
- Applications compatibles TSF, clones
- clones
- Text Services Framework (TSF), sauvegardes
- TSF (Text Services Framework), sauvegardes
- services de texte, sauvegardes
- Applications compatibles TSF, sauvegardes
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940304"
---
# <a name="ranges"></a><span data-ttu-id="3a8e4-123">Plages</span><span class="sxs-lookup"><span data-stu-id="3a8e4-123">Ranges</span></span>

## <a name="anchors"></a><span data-ttu-id="3a8e4-124">Ancres</span><span class="sxs-lookup"><span data-stu-id="3a8e4-124">Anchors</span></span>

<span data-ttu-id="3a8e4-125">Une plage est délimitée par deux points d' *ancrage*, un point d’ancrage de début et un point d’ancrage de fin.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-125">A range is delimited by two *anchors*, a start anchor and an end anchor.</span></span> <span data-ttu-id="3a8e4-126">Une ancre existe dans un emplacement imaginaire entre deux caractères.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-126">An anchor exists in an imaginary slot between two characters.</span></span> <span data-ttu-id="3a8e4-127">L’ancre de début se réfère au texte qui suit l’ancre et le point d’ancrage de fin est associé au texte qui précède l’ancre.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-127">The start anchor relates to text that follows the anchor and the end anchor relates to text that precedes the anchor.</span></span> <span data-ttu-id="3a8e4-128">Les ancres de début et de fin peuvent se trouver au même emplacement.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-128">Both the start and end anchors can exist in the same location.</span></span> <span data-ttu-id="3a8e4-129">Dans ce cas, la plage a une longueur de zéro.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-129">In this case, the range has zero length.</span></span>

<span data-ttu-id="3a8e4-130">Par exemple, commencez par le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-130">For example, start with the following text:</span></span>


```C++
This is text.
```



<span data-ttu-id="3a8e4-131">Appliquez à présent une plage à ce texte avec les ancres de début et de fin à la position 0.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-131">Now apply a range to this text with both the start and end anchors at position 0.</span></span> <span data-ttu-id="3a8e4-132">Il est représenté visuellement de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-132">It is visually represented as:</span></span>


```C++
<anchor></anchor>This is text.
```



<span data-ttu-id="3a8e4-133">Les ancres n’occupent pas d’espace dans le texte proprement dit.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-133">The anchors do not take up any space within the text itself.</span></span> <span data-ttu-id="3a8e4-134">Il s’agit d’une plage de longueur nulle et son texte est vide.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-134">This is a zero-length range and its text is empty.</span></span>

<span data-ttu-id="3a8e4-135">Décalez à présent l’ancrage de fin + 3 positions.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-135">Now shift the end anchor +3 positions.</span></span> <span data-ttu-id="3a8e4-136">Il est représenté visuellement de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-136">It is visually represented as:</span></span>


```C++
<anchor>Thi</anchor>s is text.
```



<span data-ttu-id="3a8e4-137">L’ancre de début est positionnée juste avant le caractère de la position 0 et l’ancre de fin est positionnée juste après le caractère de la position 3, car l’ancrage de fin est déplacé vers la droite de 3 endroits.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-137">The start anchor is positioned just before the character in position 0 and the end anchor is positioned just after the character in position 3 because the end anchor moved to the right 3 places.</span></span> <span data-ttu-id="3a8e4-138">La plage de texte est désormais « Thi ».</span><span class="sxs-lookup"><span data-stu-id="3a8e4-138">The range of text is now "Thi".</span></span>

<span data-ttu-id="3a8e4-139">En outre, l’ancre de début ne peut pas être effectuée pour suivre l’ancre de fin et l’ancre de fin ne peut pas être précédée de l’ancre de début.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-139">Additionally, the start anchor cannot be made to follow the end anchor and the end anchor cannot be made to precede the start anchor.</span></span>

## <a name="anchor-gravity"></a><span data-ttu-id="3a8e4-140">Gravité d’ancrage</span><span class="sxs-lookup"><span data-stu-id="3a8e4-140">Anchor Gravity</span></span>

<span data-ttu-id="3a8e4-141">Chaque ancre a un paramètre de *gravité* qui détermine le mode de réponse de l’ancre quand du texte est inséré dans le flux de texte à la position d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-141">Each anchor has a *gravity* setting that determines how the anchor responds when text is inserted into the text stream at the anchor position.</span></span> <span data-ttu-id="3a8e4-142">Lorsqu’une insertion est effectuée à la position d’un point d’ancrage, un ajustement doit être effectué à la position de l’ancre.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-142">When an insertion is made at the position of an anchor, an adjustment must be made in the position of the anchor.</span></span> <span data-ttu-id="3a8e4-143">La gravité détermine la façon dont ce réglage de la position d’ancrage est effectué.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-143">The gravity determines how this anchor position adjustment is made.</span></span>

<span data-ttu-id="3a8e4-144">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-144">For example:</span></span>


```C++
It is <anchor></anchor>cold today.
```



<span data-ttu-id="3a8e4-145">Si le mot « très » est inséré à la position de la plage, l’ancre de début peut être positionnée avant ou après le mot inséré :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-145">If the word "very " is inserted at the range position, the start anchor can be positioned either before or after the inserted word:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="3a8e4-146">\- Ou -</span><span class="sxs-lookup"><span data-stu-id="3a8e4-146">\- Or -</span></span>


```C++
It is very <anchor></anchor>cold today.
```



<span data-ttu-id="3a8e4-147">La gravité d’ancrage spécifie la manière dont l’ancrage est repositionné lorsqu’une insertion est effectuée à sa position.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-147">The anchor gravity specifies how the anchor is repositioned when an insertion is made at its position.</span></span> <span data-ttu-id="3a8e4-148">La gravité peut être vers l' *arrière* ou *vers l’avant*.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-148">The gravity can be either *backward* or *forward*.</span></span>

<span data-ttu-id="3a8e4-149">Si l’ancrage a une gravité descendante, l’ancre se déplace vers l’arrière par rapport au point d’insertion, à l’insertion, de sorte que le texte inséré suit le point d’ancrage :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-149">If the anchor has backward gravity, the anchor moves backward, relative to the insertion point, on insertion so that the inserted text follows the anchor:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="3a8e4-150">Si le point d’ancrage a une gravité en avant, l’ancrage avance (par rapport au point d’insertion) à l’insertion, de sorte que le texte inséré précède l’ancre :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-150">If the anchor has forward gravity, the anchor moves forward (relative to the insertion point) on insertion so that the inserted text precedes the anchor:</span></span>


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a><span data-ttu-id="3a8e4-151">Clones et sauvegardes</span><span class="sxs-lookup"><span data-stu-id="3a8e4-151">Clones and Backups</span></span>

<span data-ttu-id="3a8e4-152">Il existe deux façons de créer une « copie » d’un objet Range.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-152">There are two ways to make a "copy" of a range object.</span></span> <span data-ttu-id="3a8e4-153">La première consiste à créer un *clone* de la plage à l’aide de [ITfRange :: Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span><span class="sxs-lookup"><span data-stu-id="3a8e4-153">The first is to make a *clone* of the range using [ITfRange::Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span></span> <span data-ttu-id="3a8e4-154">La seconde consiste à effectuer une *sauvegarde* de la plage à l’aide de [ITfContext :: CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span><span class="sxs-lookup"><span data-stu-id="3a8e4-154">The second is to make a *backup* of the range using [ITfContext::CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span></span>

<span data-ttu-id="3a8e4-155">Un clone est une copie d’une plage qui n’inclut pas de données statiques.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-155">A clone is a copy of a range that does not include static data.</span></span> <span data-ttu-id="3a8e4-156">Les ancres de la plage sont copiées, mais le clone couvre toujours une plage de texte dans le contexte.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-156">The anchors of the range are copied, but the clone still covers a range of text within the context.</span></span> <span data-ttu-id="3a8e4-157">Un clone est un objet Range à tous égards.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-157">A clone is a range object in all respects.</span></span> <span data-ttu-id="3a8e4-158">Cela signifie que le texte et les propriétés d’une plage clonée sont dynamiques et changent si le texte et/ou les propriétés de la plage couverte par le clone changent.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-158">This means that the text and properties for a cloned range are dynamic and will change if the text and/or properties of the range covered by the clone changes.</span></span>

<span data-ttu-id="3a8e4-159">Une sauvegarde stocke le texte et les propriétés d’une plage au moment où la sauvegarde est effectuée sous forme de données statiques.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-159">A backup stores the text and properties of a range at the time the backup is made as static data.</span></span> <span data-ttu-id="3a8e4-160">Une sauvegarde clone également la plage d’origine afin que les modifications apportées à la taille et à la position de la plage d’origine puissent être suivies.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-160">A backup also clones the original range so that changes to the size and position of the original range can be tracked.</span></span> <span data-ttu-id="3a8e4-161">Cela signifie que le texte et les propriétés d’une plage sauvegardée sont statiques et ne changent pas si le texte et/ou les propriétés de la plage couverte par la sauvegarde sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-161">This means that the text and properties for a backed up range are static and do not change if the text and/or properties of the range covered by the backup changes.</span></span>

<span data-ttu-id="3a8e4-162">Par exemple, la plage suivante (pRange) dans le contexte :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-162">For example, the following range (pRange) within the context:</span></span>


```C++
"This is some <pRange>text</pRange>."
```



<span data-ttu-id="3a8e4-163">Créez maintenant un clone et une sauvegarde de cette plage :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-163">Now make a clone and a backup of this range:</span></span>


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



<span data-ttu-id="3a8e4-164">À présent, les objets contiennent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-164">Now, the objects contain the following:</span></span>


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="3a8e4-165">À présent, modifiez le texte de pRange :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-165">Now change the text of pRange:</span></span>


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



<span data-ttu-id="3a8e4-166">À présent, les objets contiennent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-166">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="3a8e4-167">La définition du texte a entraîné la modification du texte dans le contexte.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-167">Setting the text caused the text within the context to change.</span></span> <span data-ttu-id="3a8e4-168">Elle a également provoqué la modification de l’ancre de fin de pRange et pClone.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-168">It also caused the end anchor of pRange and pClone to change.</span></span> <span data-ttu-id="3a8e4-169">pClone contient maintenant « other words », car le texte a été modifié dans la plage et ces modifications sont suivies par toutes les plages.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-169">pClone now contains "other words" because the text changed within the range and these changes are tracked by all ranges.</span></span> <span data-ttu-id="3a8e4-170">Lorsque le texte couvert à la fois par pRange et pClone a changé, le texte de pClone a également changé.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-170">When the text covered by both pRange and pClone changed, the text of pClone changed as well.</span></span>

<span data-ttu-id="3a8e4-171">Le texte dans pBackup n’a pas été modifié par rapport au pRange d’origine, car les données (texte et propriétés) de la sauvegarde ne sont pas liées au contexte et sont stockées séparément.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-171">The text in pBackup has not changed from the original pRange because the data (text and properties) in the backup is unrelated to the context and is stored separately.</span></span> <span data-ttu-id="3a8e4-172">Le clone contenu dans la sauvegarde change en réalité, mais les données sont statiques.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-172">The clone contained within the backup does actually change, but the data is static.</span></span>

<span data-ttu-id="3a8e4-173">Lors de la restauration d’une sauvegarde, la sauvegarde peut être appliquée au clone au sein de la sauvegarde ou à une plage différente.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-173">When restoring a backup, the backup can be applied to the clone within the backup or to a different range entirely.</span></span> <span data-ttu-id="3a8e4-174">Pour appliquer la sauvegarde au clone au sein de la sauvegarde, transmettez la **valeur null** à [ITfRangeBackup :: Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) , comme indiqué dans l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-174">To apply the backup to the clone within the backup, pass **NULL** to [ITfRangeBackup::Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) as shown in the following code example:</span></span>


```C++
pBackup->Restore(ec, NULL);
```



<span data-ttu-id="3a8e4-175">À présent, les objets contiennent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-175">Now, the objects contain the following:</span></span>


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="3a8e4-176">Pour restaurer la sauvegarde dans une autre plage, transmettez un pointeur vers l’objet Range lors de l’appel de **ITfRangeBackup :: Restore**.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-176">To restore the backup to a different range, pass a pointer to the range object when calling **ITfRangeBackup::Restore**.</span></span> <span data-ttu-id="3a8e4-177">Le texte et les propriétés sauvegardés seront appliqués à la nouvelle plage.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-177">The backed up text and properties will be applied to the new range.</span></span> <span data-ttu-id="3a8e4-178">Par exemple, à l’aide de l’exemple ci-dessus, avant l’appel **Restore** , Prange sera modifié pour illustrer ceci :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-178">For example, using the example above prior to the **Restore** call, pRange will be modified to demonstrate this:</span></span>


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



<span data-ttu-id="3a8e4-179">À présent, les objets contiennent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-179">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="3a8e4-180">Lorsque l’ancrage de fin de pRange a été déplacé vers les deux emplacements de gauche, l’ancrage de fin de pClone n’a pas changé.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-180">When the end anchor of pRange was shifted to the left two places, the end anchor of pClone did not change.</span></span>

<span data-ttu-id="3a8e4-181">À présent, restaurez la sauvegarde à l’aide de pRange avec l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-181">Now restore the backup using pRange with the following code example:</span></span>


```C++
pBackup->Restore(ec, pRange);
```



<span data-ttu-id="3a8e4-182">À présent, les objets contiennent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3a8e4-182">Now, the objects contain the following:</span></span>


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



<span data-ttu-id="3a8e4-183">Le texte couvert par pRange a été remplacé par « Text », une partie du texte couvert par pClone a changé et pBackup change pour correspondre à pRange.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-183">The text covered by pRange has been replaced with "text", a portion of the text covered by pClone has changed, and pBackup changes to match pRange.</span></span>

 

 




