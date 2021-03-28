---
description: Utilisez les constantes suivantes pour identifier la session de journalisation du noyau NT.
ms.assetid: f64f05c1-b904-4847-8502-4abb9cf4d37f
title: Constantes d’enregistreur de noyau NT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13767400ff851e358f6665c88e16767cc378a4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973718"
---
# <a name="nt-kernel-logger-constants"></a><span data-ttu-id="aa795-103">Constantes d’enregistreur de noyau NT</span><span class="sxs-lookup"><span data-stu-id="aa795-103">NT Kernel Logger Constants</span></span>

<span data-ttu-id="aa795-104">Utilisez les constantes suivantes pour identifier la session de journalisation du noyau NT.</span><span class="sxs-lookup"><span data-stu-id="aa795-104">Use the following constants to identify the NT Kernel Logger session.</span></span>



| <span data-ttu-id="aa795-105">Constante</span><span class="sxs-lookup"><span data-stu-id="aa795-105">Constant</span></span>               | <span data-ttu-id="aa795-106">Description</span><span class="sxs-lookup"><span data-stu-id="aa795-106">Description</span></span>                                                      |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="aa795-107">SystemTraceControlGuid</span><span class="sxs-lookup"><span data-stu-id="aa795-107">SystemTraceControlGuid</span></span> | <span data-ttu-id="aa795-108">GUID de contrôle pour la session de suivi d’événements du journal de noyau NT.</span><span class="sxs-lookup"><span data-stu-id="aa795-108">The control GUID for the NT Kernel Logger event tracing session.</span></span> |
| <span data-ttu-id="aa795-109">\_nom du journal du noyau \_</span><span class="sxs-lookup"><span data-stu-id="aa795-109">KERNEL\_LOGGER\_NAME</span></span>   | <span data-ttu-id="aa795-110">Nom de la session de suivi d’événements du journal de noyau NT.</span><span class="sxs-lookup"><span data-stu-id="aa795-110">The name of the NT Kernel Logger event tracing session.</span></span>          |



 

<span data-ttu-id="aa795-111">La session du journal de noyau NT est la seule session qui peut accepter des événements des fournisseurs d’événements du noyau.</span><span class="sxs-lookup"><span data-stu-id="aa795-111">The NT Kernel Logger session is the only session that can accept events from kernel event providers.</span></span> <span data-ttu-id="aa795-112">La session d’enregistrement de noyau NT n’accepte pas les événements d’autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="aa795-112">The NT Kernel Logger session does not accept events from other providers.</span></span> <span data-ttu-id="aa795-113">Si vous souhaitez capturer des événements de noyau et des événements à partir d’autres fournisseurs, vous devez utiliser deux sessions distinctes et le consommateur doit fusionner les événements des fichiers journaux pour fournir des résultats de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="aa795-113">If you want to capture kernel events and events from other providers, you must use two separate sessions and the consumer would need to merge the events from the log files to provide end-to-end results.</span></span>

<span data-ttu-id="aa795-114">ETW utilise la macro définir le \_ GUID pour définir des GUID.</span><span class="sxs-lookup"><span data-stu-id="aa795-114">ETW uses the DEFINE\_GUID macro to define GUIDs.</span></span> <span data-ttu-id="aa795-115">Pour utiliser **SystemTraceControlGuid** dans votre code, vous devez inclure \# define INITGUID avant d’inclure Evntrace. h.</span><span class="sxs-lookup"><span data-stu-id="aa795-115">To use **SystemTraceControlGuid** in your code, you must include \#define INITGUID before including Evntrace.h.</span></span> <span data-ttu-id="aa795-116">Le compilateur transforme alors le GUID de définition \_ en GUID constant.</span><span class="sxs-lookup"><span data-stu-id="aa795-116">The compiler will then turn the DEFINE\_GUID into a constant GUID.</span></span>

<span data-ttu-id="aa795-117">Les valeurs suivantes définissent les GUID de classe possibles pour les événements de noyau qu’une session de journalisation de noyau NT peut suivre.</span><span class="sxs-lookup"><span data-stu-id="aa795-117">The following values define the possible class GUIDs for kernel events that an NT Kernel Logger session can trace.</span></span> <span data-ttu-id="aa795-118">Vous pouvez transmettre les GUID de classe à la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) pour configurer un traitement spécial pour chaque classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="aa795-118">You can pass the class GUIDs to the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function to set up special processing for each event class.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa795-119">Classe</span><span class="sxs-lookup"><span data-stu-id="aa795-119">Class</span></span></th>
<th><span data-ttu-id="aa795-120">GUID</span><span class="sxs-lookup"><span data-stu-id="aa795-120">GUID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa795-121"><a href="alpc.md"><strong>ALPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-121"><a href="alpc.md"><strong>ALPC</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 45d8cccd-539f-4b72-a8b7-5c683142609a */
    ALPCGuid,
    0x45d8cccd,
    0x539f,
    0x4b72,
    0xa8, 0xb7, 0x5c, 0x68, 0x31, 0x42, 0x60, 0x9a
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa795-122"><a href="diskio.md"><strong>E</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-122"><a href="diskio.md"><strong>DiskIo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c */
    DiskIoGuid,
    0x3d6fa8d4,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa795-123"><a href="hwconfig.md"><strong>HWConfig</strong></a> et <a href="systemconfig.md"> <strong>SystemConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-123"><a href="hwconfig.md"><strong>HWConfig</strong></a> and <a href="systemconfig.md"><strong>SystemConfig</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 01853a65-418f-4f36-aefc-dc0f1d2fd235 */
    EventTraceConfigGuid,
    0x01853a65,
    0x418f,
    0x4f36,
    0xae, 0xfc, 0xdc, 0x0f, 0x1d, 0x2f, 0xd2, 0x35
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa795-124"><a href="fileio.md"><strong>FileIo</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-124"><a href="fileio.md"><strong>FileIo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 90cbdc39-4a3e-11d1-84f4-0000f80464e3 */
    FileIoGuid,
    0x90cbdc39,
    0x4a3e,
    0x11d1,
    0x84, 0xf4, 0x00, 0x00, 0xf8, 0x04, 0x64, 0xe3
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa795-125"><a href="image.md"><strong>Image</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-125"><a href="image.md"><strong>Image</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 2cb15d1d-5fc1-11d2-abe1-00a0c911f518 */
    ImageLoadGuid,
    0x2cb15d1d,
    0x5fc1,
    0x11d2,
    0xab, 0xe1, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x18
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa795-126"><a href="pagefault-v2.md"><strong>PageFault_V2</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-126"><a href="pagefault-v2.md"><strong>PageFault_V2</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c */
    PageFaultGuid,
    0x3d6fa8d3,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa795-127"><a href="perfinfo.md"><strong>PerfInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-127"><a href="perfinfo.md"><strong>PerfInfo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* ce1dbfb4-137e-4da6-87b0-3f59aa102cbc */
    PerfInfoGuid,
    0xce1dbfb4,
    0x137e,
    0x4da6,
    0x87, 0xb0, 0x3f, 0x59, 0xaa, 0x10, 0x2c, 0xbc
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa795-128"><a href="process.md"><strong>Processus</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-128"><a href="process.md"><strong>Process</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c */
    ProcessGuid,
    0x3d6fa8d0,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa795-129"><a href="registry.md"><strong>Registre</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-129"><a href="registry.md"><strong>Registry</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* AE53722E-C863-11d2-8659-00C04FA321A1 */
    RegistryGuid, 
    0xae53722e,
    0xc863,
    0x11d2,
    0x86, 0x59, 0x0, 0xc0, 0x4f, 0xa3, 0x21, 0xa1
);</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa795-130"><a href="splitio.md"><strong>SplitIo</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-130"><a href="splitio.md"><strong>SplitIo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* d837ca92-12b9-44a5-ad6a-3a65b3578aa8 */
    SplitIoGuid, 
    0xd837ca92,
    0x12b9,
    0x44a5,
    0xad, 0x6a, 0x3a, 0x65, 0xb3, 0x57, 0x8a, 0xa8
);</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa795-131"><a href="tcpip.md"><strong>Msafd</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-131"><a href="tcpip.md"><strong>TcpIp</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 9a280ac0-c8e0-11d1-84e2-00c04fb998a2 */
    TcpIpGuid,
    0x9a280ac0,
    0xc8e0,
    0x11d1,
    0x84, 0xe2, 0x00, 0xc0, 0x4f, 0xb9, 0x98, 0xa2
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa795-132"><a href="thread.md"><strong>Thread</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-132"><a href="thread.md"><strong>Thread</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c */
    ThreadGuid,
    0x3d6fa8d1,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa795-133"><a href="udpip.md"><strong>UdpIp</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa795-133"><a href="udpip.md"><strong>UdpIp</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* bf3a50c5-a9c9-4988-a005-2df0b7c80f80 */
    UdpIpGuid,
    0xbf3a50c5,
    0xa9c9,
    0x4988,
    0xa0, 0x05, 0x2d, 0xf0, 0xb7, 0xc8, 0x0f, 0x80
  );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="aa795-134">Notes</span><span class="sxs-lookup"><span data-stu-id="aa795-134">Remarks</span></span>

<span data-ttu-id="aa795-135">Pour utiliser les GUID, copiez les définitions de GUID que vous souhaitez utiliser dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="aa795-135">To use the GUIDs, copy the GUID definitions that you want to use to your source code.</span></span> <span data-ttu-id="aa795-136">Vous devez inclure \# define INITGUID avant les définitions que vous incluez dans votre code source, afin que le compilateur transforme le GUID de définition \_ en GUID constant.</span><span class="sxs-lookup"><span data-stu-id="aa795-136">You must include \#define INITGUID before the definitions you include in your source code, so the compiler will turn the DEFINE\_GUID into a constant GUID.</span></span> <span data-ttu-id="aa795-137">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="aa795-137">For example,</span></span>

``` syntax
#define INITGUID

DEFINE_GUID ( /* 3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c */
    ThreadGuid,
    0x3d6fa8d1,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );

DEFINE_GUID ( /* 3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c */
    ProcessGuid,
    0x3d6fa8d0,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );
```

<span data-ttu-id="aa795-138">Comme alternative, vous pouvez définir vous-même le GUID constant pour les définitions de GUID.</span><span class="sxs-lookup"><span data-stu-id="aa795-138">As an alternative, you can define the constant GUID for the GUID definitions yourself.</span></span> <span data-ttu-id="aa795-139">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="aa795-139">For example,</span></span>

``` syntax
static const GUID ThreadGuid = 
{ 0x3d6fa8d0, 0xfe05, 0x11d0, { 0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c } };
```

 

 
