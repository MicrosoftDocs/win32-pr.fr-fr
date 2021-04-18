---
title: Structure RAS_PORT_STATISTICS (rassapi. h)
description: La \_ structure des statistiques du port RAS \_ signale les statistiques collectées par un serveur RAS pour un port connecté.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS_PORT_STATISTICS de la structure RAS
- Point d’accès RAS du pointeur de structure PRAS_PORT_STATISTICS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512397"
---
# <a name="ras_port_statistics-structure"></a><span data-ttu-id="769a8-105">Structure des statistiques du \_ port RAS \_</span><span class="sxs-lookup"><span data-stu-id="769a8-105">RAS\_PORT\_STATISTICS structure</span></span>

<span data-ttu-id="769a8-106">\[La structure des **\_ \_ statistiques du port RAS** n’est pas prise en charge par Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="769a8-106">\[The **RAS\_PORT\_STATISTICS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="769a8-107">La structure des **\_ \_ statistiques du port RAS** signale les statistiques collectées par un serveur RAS pour un port connecté.</span><span class="sxs-lookup"><span data-stu-id="769a8-107">The **RAS\_PORT\_STATISTICS** structure reports the statistics that a RAS server collects for a connected port.</span></span> <span data-ttu-id="769a8-108">Le serveur RAS réinitialise les différents compteurs de statistiques chaque fois que le port est connecté.</span><span class="sxs-lookup"><span data-stu-id="769a8-108">The RAS server resets the various statistic counters each time the port is connected.</span></span> <span data-ttu-id="769a8-109">Appelez la fonction [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) pour forcer le serveur RAS à réinitialiser les compteurs des statistiques.</span><span class="sxs-lookup"><span data-stu-id="769a8-109">Call the [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) function to force the RAS server to reset the statistic counters.</span></span>

<span data-ttu-id="769a8-110">Pour un port qui fait partie d’une connexion à liaisons multiples, cette structure fournit deux ensembles de statistiques.</span><span class="sxs-lookup"><span data-stu-id="769a8-110">For a port that is part of a multilink connection, this structure provides two sets of statistics.</span></span> <span data-ttu-id="769a8-111">Le premier jeu contient les statistiques cumulatives pour tous les ports de la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-111">The first set contains the cumulative statistics for all ports in the connection.</span></span> <span data-ttu-id="769a8-112">Ces statistiques sont les mêmes pour tous les ports de la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-112">These statistics are the same for all ports in the connection.</span></span> <span data-ttu-id="769a8-113">Le deuxième jeu contient les statistiques de ce port uniquement.</span><span class="sxs-lookup"><span data-stu-id="769a8-113">The second set contains the statistics for just this port.</span></span> <span data-ttu-id="769a8-114">Si le port ne fait pas partie d’une connexion multilien, les deux ensembles de statistiques ont les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="769a8-114">If the port is not part of a multilink connection, both sets of statistics have the same information.</span></span> <span data-ttu-id="769a8-115">Pour déterminer si un port fait partie d’une connexion multilien, vérifiez le \_ bit de liaison multilien dans le membre **Flags** de la structure [**du \_ port RAS \_ 0**](ras-port-0-str.md) du port.</span><span class="sxs-lookup"><span data-stu-id="769a8-115">To determine whether a port is part of a multilink connection, check the PORT\_MULTILINKED bit in the **Flags** member of the port's [**RAS\_PORT\_0**](ras-port-0-str.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="769a8-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="769a8-116">Syntax</span></span>


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a><span data-ttu-id="769a8-117">Membres</span><span class="sxs-lookup"><span data-stu-id="769a8-117">Members</span></span>

<dl> <dt>

<span data-ttu-id="769a8-118">**dwBytesXmited**</span><span class="sxs-lookup"><span data-stu-id="769a8-118">**dwBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-119">Spécifie le nombre total d’octets transmis par la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-119">Specifies the total number of bytes transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-120">**dwBytesRcved**</span><span class="sxs-lookup"><span data-stu-id="769a8-120">**dwBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-121">Spécifie le nombre total d’octets reçus par la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-121">Specifies the total number of bytes received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-122">**dwFramesXmited**</span><span class="sxs-lookup"><span data-stu-id="769a8-122">**dwFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-123">Spécifie le nombre total de trames transmises par la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-123">Specifies the total number of frames transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-124">**dwFramesRcved**</span><span class="sxs-lookup"><span data-stu-id="769a8-124">**dwFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-125">Spécifie le nombre total de trames reçues par la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-125">Specifies the total number of frames received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-126">**dwCrcErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-126">**dwCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-127">Spécifie le nombre total d’erreurs CRC sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-127">Specifies the total number of CRC errors on the connection.</span></span> <span data-ttu-id="769a8-128">Les erreurs CRC sont provoquées par l’échec d’une vérification de redondance cyclique.</span><span class="sxs-lookup"><span data-stu-id="769a8-128">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="769a8-129">Une erreur CRC indique qu’un ou plusieurs caractères du paquet de données reçus ont été détectés comme étant déformés à l’arrivée.</span><span class="sxs-lookup"><span data-stu-id="769a8-129">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-130">**dwTimeoutErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-130">**dwTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-131">Spécifie le nombre total d’erreurs de délai d’attente sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-131">Specifies the total number of time-out errors on the connection.</span></span> <span data-ttu-id="769a8-132">Des erreurs de délai d’attente se produisent lorsqu’un caractère attendu n’est pas reçu dans le temps.</span><span class="sxs-lookup"><span data-stu-id="769a8-132">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="769a8-133">Dans ce cas, le logiciel suppose que les données ont été perdues et demande qu’il soit renvoyé.</span><span class="sxs-lookup"><span data-stu-id="769a8-133">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-134">**dwAlignmentErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-134">**dwAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-135">Spécifie le nombre total d’erreurs d’alignement sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-135">Specifies the total number of alignment errors on the connection.</span></span> <span data-ttu-id="769a8-136">Des erreurs d’alignement se produisent lorsqu’un caractère reçu n’est pas celui attendu.</span><span class="sxs-lookup"><span data-stu-id="769a8-136">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="769a8-137">Cela se produit généralement lorsqu’un caractère est perdu ou lorsqu’une erreur de délai d’attente se produit.</span><span class="sxs-lookup"><span data-stu-id="769a8-137">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-138">**dwHardwareOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-138">**dwHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-139">Spécifie le nombre total d’erreurs de saturation matérielle sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-139">Specifies the total number of hardware overrun errors on the connection.</span></span> <span data-ttu-id="769a8-140">Ces erreurs indiquent le nombre de fois que l’ordinateur expéditeur a transmis des caractères plus rapidement que le matériel de l’ordinateur récepteur peut les traiter.</span><span class="sxs-lookup"><span data-stu-id="769a8-140">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="769a8-141">Si ce problème persiste, réduisez la vitesse de connexion BPS sur le client.</span><span class="sxs-lookup"><span data-stu-id="769a8-141">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-142">**dwFramingErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-142">**dwFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-143">Spécifie le nombre total d’erreurs de tramage sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-143">Specifies the total number of framing errors on the connection.</span></span> <span data-ttu-id="769a8-144">Une erreur de trame se produit lorsqu’un caractère asynchrone est reçu avec un bit de démarrage ou d’arrêt non valide.</span><span class="sxs-lookup"><span data-stu-id="769a8-144">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-145">**dwBufferOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-145">**dwBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-146">Spécifie le nombre total d’erreurs de dépassement de mémoire tampon sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-146">Specifies the total number of buffer overrun errors on the connection.</span></span> <span data-ttu-id="769a8-147">Une erreur de dépassement de mémoire tampon se produit lorsque l’ordinateur expéditeur transmet des caractères plus rapidement que l’ordinateur récepteur ne peut les gérer.</span><span class="sxs-lookup"><span data-stu-id="769a8-147">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="769a8-148">Si ce problème persiste, réduisez la vitesse de connexion BPS sur le client.</span><span class="sxs-lookup"><span data-stu-id="769a8-148">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-149">**dwBytesXmitedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="769a8-149">**dwBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-150">Spécifie le nombre total d’octets transmis non compressés par la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-150">Specifies the total number of bytes transmitted uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-151">**dwBytesRcvedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="769a8-151">**dwBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-152">Spécifie le nombre total d’octets reçus non compressés par la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-152">Specifies the total number of bytes received uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-153">**dwBytesXmitedCompressed**</span><span class="sxs-lookup"><span data-stu-id="769a8-153">**dwBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-154">Spécifie le nombre total d’octets transmis compressés par la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-154">Specifies the total number of bytes transmitted compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-155">**dwBytesRcvedCompressed**</span><span class="sxs-lookup"><span data-stu-id="769a8-155">**dwBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-156">Spécifie le nombre total d’octets reçus compressés par la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-156">Specifies the total number of bytes received compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-157">**dwPortBytesXmited**</span><span class="sxs-lookup"><span data-stu-id="769a8-157">**dwPortBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-158">Spécifie le nombre total d’octets transmis par le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-158">Specifies the total number of bytes transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-159">**dwPortBytesRcved**</span><span class="sxs-lookup"><span data-stu-id="769a8-159">**dwPortBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-160">Spécifie le nombre total d’octets reçus par le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-160">Specifies the total number of bytes received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-161">**dwPortFramesXmited**</span><span class="sxs-lookup"><span data-stu-id="769a8-161">**dwPortFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-162">Spécifie le nombre total de trames transmises par le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-162">Specifies the total number of frames transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-163">**dwPortFramesRcved**</span><span class="sxs-lookup"><span data-stu-id="769a8-163">**dwPortFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-164">Spécifie le nombre total de trames reçues par le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-164">Specifies the total number of frames received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-165">**dwPortCrcErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-165">**dwPortCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-166">Spécifie le nombre total d’erreurs CRC sur le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-166">Specifies the total number of CRC errors on the port.</span></span> <span data-ttu-id="769a8-167">Les erreurs CRC sont provoquées par l’échec d’une vérification de redondance cyclique.</span><span class="sxs-lookup"><span data-stu-id="769a8-167">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="769a8-168">Une erreur CRC indique qu’un ou plusieurs caractères du paquet de données reçus ont été détectés comme étant déformés à l’arrivée.</span><span class="sxs-lookup"><span data-stu-id="769a8-168">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-169">**dwPortTimeoutErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-169">**dwPortTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-170">Spécifie le nombre total d’erreurs de délai d’attente sur le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-170">Specifies the total number of time-out errors on the port.</span></span> <span data-ttu-id="769a8-171">Des erreurs de délai d’attente se produisent lorsqu’un caractère attendu n’est pas reçu dans le temps.</span><span class="sxs-lookup"><span data-stu-id="769a8-171">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="769a8-172">Dans ce cas, le logiciel suppose que les données ont été perdues et demande qu’il soit renvoyé.</span><span class="sxs-lookup"><span data-stu-id="769a8-172">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-173">**dwPortAlignmentErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-173">**dwPortAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-174">Spécifie le nombre total d’erreurs d’alignement sur le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-174">Specifies the total number of alignment errors on the port.</span></span> <span data-ttu-id="769a8-175">Des erreurs d’alignement se produisent lorsqu’un caractère reçu n’est pas celui attendu.</span><span class="sxs-lookup"><span data-stu-id="769a8-175">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="769a8-176">Cela se produit généralement lorsqu’un caractère est perdu ou lorsqu’une erreur de délai d’attente se produit.</span><span class="sxs-lookup"><span data-stu-id="769a8-176">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-177">**dwPortHardwareOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-177">**dwPortHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-178">Spécifie le nombre total d’erreurs de saturation matérielle sur le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-178">Specifies the total number of hardware overrun errors on the port.</span></span> <span data-ttu-id="769a8-179">Ces erreurs indiquent le nombre de fois que l’ordinateur expéditeur a transmis des caractères plus rapidement que le matériel de l’ordinateur récepteur peut les traiter.</span><span class="sxs-lookup"><span data-stu-id="769a8-179">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="769a8-180">Si ce problème persiste, réduisez la vitesse de connexion BPS sur le client.</span><span class="sxs-lookup"><span data-stu-id="769a8-180">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-181">**dwPortFramingErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-181">**dwPortFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-182">Spécifie le nombre total d’erreurs de tramage sur le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-182">Specifies the total number of framing errors on the port.</span></span> <span data-ttu-id="769a8-183">Une erreur de trame se produit lorsqu’un caractère asynchrone est reçu avec un bit de démarrage ou d’arrêt non valide.</span><span class="sxs-lookup"><span data-stu-id="769a8-183">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-184">**dwPortBufferOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="769a8-184">**dwPortBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-185">Spécifie le nombre total d’erreurs de dépassement de mémoire tampon sur le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-185">Specifies the total number of buffer overrun errors on the port.</span></span> <span data-ttu-id="769a8-186">Une erreur de dépassement de mémoire tampon se produit lorsque l’ordinateur expéditeur transmet des caractères plus rapidement que l’ordinateur récepteur ne peut les gérer.</span><span class="sxs-lookup"><span data-stu-id="769a8-186">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="769a8-187">Si ce problème persiste, réduisez la vitesse de connexion BPS sur le client.</span><span class="sxs-lookup"><span data-stu-id="769a8-187">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-188">**dwPortBytesXmitedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="769a8-188">**dwPortBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-189">Spécifie le nombre total d’octets transmis non compressés par le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-189">Specifies the total number of bytes transmitted uncompressed by the port.</span></span> <span data-ttu-id="769a8-190">Si le port fait partie d’une connexion multilien, ce membre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="769a8-190">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="769a8-191">Utilisez plutôt les statistiques de compression pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-191">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-192">**dwPortBytesRcvedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="769a8-192">**dwPortBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-193">Spécifie le nombre total d’octets reçus non compressés par le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-193">Specifies the total number of bytes received uncompressed by the port.</span></span> <span data-ttu-id="769a8-194">Si le port fait partie d’une connexion multilien, ce membre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="769a8-194">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="769a8-195">Utilisez plutôt les statistiques de compression pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-195">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-196">**dwPortBytesXmitedCompressed**</span><span class="sxs-lookup"><span data-stu-id="769a8-196">**dwPortBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-197">Spécifie le nombre total d’octets transmis compressés par le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-197">Specifies the total number of bytes transmitted compressed by the port.</span></span> <span data-ttu-id="769a8-198">Si le port fait partie d’une connexion multilien, ce membre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="769a8-198">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="769a8-199">Utilisez plutôt les statistiques de compression pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-199">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="769a8-200">**dwPortBytesRcvedCompressed**</span><span class="sxs-lookup"><span data-stu-id="769a8-200">**dwPortBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="769a8-201">Spécifie le nombre total d’octets reçus compressés par le port.</span><span class="sxs-lookup"><span data-stu-id="769a8-201">Specifies the total number of bytes received compressed by the port.</span></span> <span data-ttu-id="769a8-202">Si le port fait partie d’une connexion multilien, ce membre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="769a8-202">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="769a8-203">Utilisez plutôt les statistiques de compression pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="769a8-203">Use the compression statistics for the connection instead.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="769a8-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="769a8-204">Requirements</span></span>



| <span data-ttu-id="769a8-205">Condition requise</span><span class="sxs-lookup"><span data-stu-id="769a8-205">Requirement</span></span> | <span data-ttu-id="769a8-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="769a8-206">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="769a8-207">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="769a8-207">Minimum supported client</span></span><br/> | <span data-ttu-id="769a8-208">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="769a8-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="769a8-209">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="769a8-209">Minimum supported server</span></span><br/> | <span data-ttu-id="769a8-210">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="769a8-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="769a8-211">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="769a8-211">End of client support</span></span><br/>    | <span data-ttu-id="769a8-212">Windows XP</span><span class="sxs-lookup"><span data-stu-id="769a8-212">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="769a8-213">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="769a8-213">End of server support</span></span><br/>    | <span data-ttu-id="769a8-214">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="769a8-214">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="769a8-215">En-tête</span><span class="sxs-lookup"><span data-stu-id="769a8-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="769a8-216"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="769a8-216"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="769a8-217">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="769a8-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="769a8-218">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="769a8-218">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="769a8-219">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="769a8-219">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="769a8-220">**\_Port RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="769a8-220">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="769a8-221">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="769a8-221">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="769a8-222">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="769a8-222">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="769a8-223">**RasAdminPortClearStatistics**</span><span class="sxs-lookup"><span data-stu-id="769a8-223">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)
</dt> <dt>

[<span data-ttu-id="769a8-224">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="769a8-224">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





