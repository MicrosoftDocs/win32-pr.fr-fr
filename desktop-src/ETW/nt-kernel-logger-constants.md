---
description: Utilisez les constantes suivantes pour identifier la session de journalisation du noyau NT.
ms.assetid: f64f05c1-b904-4847-8502-4abb9cf4d37f
title: Constantes d’enregistreur de noyau NT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd5b8176fb3b0ca6c63bc5a0aa3bf4bcd6d7067f4c3710a9a6e74b48603dc50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151455"
---
# <a name="nt-kernel-logger-constants"></a>Constantes d’enregistreur de noyau NT

Utilisez les constantes suivantes pour identifier la session de journalisation du noyau NT.



| Constante               | Description                                                      |
|------------------------|------------------------------------------------------------------|
| SystemTraceControlGuid | GUID de contrôle pour la session de suivi d’événements du journal de noyau NT. |
| \_nom du journal du noyau \_   | Nom de la session de suivi d’événements du journal de noyau NT.          |



 

La session du journal de noyau NT est la seule session qui peut accepter des événements des fournisseurs d’événements du noyau. La session d’enregistrement de noyau NT n’accepte pas les événements d’autres fournisseurs. Si vous souhaitez capturer des événements de noyau et des événements à partir d’autres fournisseurs, vous devez utiliser deux sessions distinctes et le consommateur doit fusionner les événements des fichiers journaux pour fournir des résultats de bout en bout.

ETW utilise la macro définir le \_ GUID pour définir des GUID. Pour utiliser **SystemTraceControlGuid** dans votre code, vous devez inclure \# define INITGUID avant d’inclure Evntrace. h. Le compilateur transforme alors le GUID de définition \_ en GUID constant.

Les valeurs suivantes définissent les GUID de classe possibles pour les événements de noyau qu’une session de journalisation de noyau NT peut suivre. Vous pouvez transmettre les GUID de classe à la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) pour configurer un traitement spécial pour chaque classe d’événements.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Classe</th>
<th>GUID</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="alpc.md"><strong>ALPC</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 45d8cccd-539f-4b72-a8b7-5c683142609a */
    ALPCGuid,
    0x45d8cccd,
    0x539f,
    0x4b72,
    0xa8, 0xb7, 0x5c, 0x68, 0x31, 0x42, 0x60, 0x9a
  );</code></pre></td>
</tr>
<tr class="even">
<td><a href="diskio.md"><strong>E</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c */
    DiskIoGuid,
    0x3d6fa8d4,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><a href="hwconfig.md"><strong>HWConfig</strong></a> et <a href="systemconfig.md"> <strong>SystemConfig</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 01853a65-418f-4f36-aefc-dc0f1d2fd235 */
    EventTraceConfigGuid,
    0x01853a65,
    0x418f,
    0x4f36,
    0xae, 0xfc, 0xdc, 0x0f, 0x1d, 0x2f, 0xd2, 0x35
  );</code></pre></td>
</tr>
<tr class="even">
<td><a href="fileio.md"><strong>FileIo</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 90cbdc39-4a3e-11d1-84f4-0000f80464e3 */
    FileIoGuid,
    0x90cbdc39,
    0x4a3e,
    0x11d1,
    0x84, 0xf4, 0x00, 0x00, 0xf8, 0x04, 0x64, 0xe3
  );</code></pre></td>
</tr>
<tr class="odd">
<td><a href="image.md"><strong>Image</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 2cb15d1d-5fc1-11d2-abe1-00a0c911f518 */
    ImageLoadGuid,
    0x2cb15d1d,
    0x5fc1,
    0x11d2,
    0xab, 0xe1, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x18
  );</code></pre></td>
</tr>
<tr class="even">
<td><a href="pagefault-v2.md"><strong>PageFault_V2</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c */
    PageFaultGuid,
    0x3d6fa8d3,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><a href="perfinfo.md"><strong>PerfInfo</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* ce1dbfb4-137e-4da6-87b0-3f59aa102cbc */
    PerfInfoGuid,
    0xce1dbfb4,
    0x137e,
    0x4da6,
    0x87, 0xb0, 0x3f, 0x59, 0xaa, 0x10, 0x2c, 0xbc
  );</code></pre></td>
</tr>
<tr class="even">
<td><a href="process.md"><strong>Processus</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c */
    ProcessGuid,
    0x3d6fa8d0,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><a href="registry.md"><strong>Registre</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* AE53722E-C863-11d2-8659-00C04FA321A1 */
    RegistryGuid, 
    0xae53722e,
    0xc863,
    0x11d2,
    0x86, 0x59, 0x0, 0xc0, 0x4f, 0xa3, 0x21, 0xa1
);</code></pre></td>
</tr>
<tr class="even">
<td><a href="splitio.md"><strong>SplitIo</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* d837ca92-12b9-44a5-ad6a-3a65b3578aa8 */
    SplitIoGuid, 
    0xd837ca92,
    0x12b9,
    0x44a5,
    0xad, 0x6a, 0x3a, 0x65, 0xb3, 0x57, 0x8a, 0xa8
);</code></pre></td>
</tr>
<tr class="odd">
<td><a href="tcpip.md"><strong>Msafd</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 9a280ac0-c8e0-11d1-84e2-00c04fb998a2 */
    TcpIpGuid,
    0x9a280ac0,
    0xc8e0,
    0x11d1,
    0x84, 0xe2, 0x00, 0xc0, 0x4f, 0xb9, 0x98, 0xa2
  );</code></pre></td>
</tr>
<tr class="even">
<td><a href="thread.md"><strong>Thread</strong></a></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c */
    ThreadGuid,
    0x3d6fa8d1,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><a href="udpip.md"><strong>UdpIp</strong></a></td>
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



 

## <a name="remarks"></a>Remarques

Pour utiliser les GUID, copiez les définitions de GUID que vous souhaitez utiliser dans votre code source. Vous devez inclure \# define INITGUID avant les définitions que vous incluez dans votre code source, afin que le compilateur transforme le GUID de définition \_ en GUID constant. Par exemple,

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

Comme alternative, vous pouvez définir vous-même le GUID constant pour les définitions de GUID. Par exemple,

``` syntax
static const GUID ThreadGuid = 
{ 0x3d6fa8d0, 0xfe05, 0x11d0, { 0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c } };
```

 

 
