import React, { useState } from "react";
import {
  Home,
  Activity,
  Users,
  Briefcase,
  Calendar,
  CheckCircle,
  Bell,
  ClipboardList,
} from "lucide-react";
import { Card, CardContent } from "@/components/ui/card";

// Recharts core imports
import {
  ResponsiveContainer,
  LineChart,
  Line,
  XAxis,
  YAxis,
  Tooltip,
  AreaChart,
  Area,
  BarChart,
  Bar,
  PieChart,
  Pie,
  FunnelChart,
  Funnel,
  Legend,
  Cell,
  LabelList,
} from "recharts";

/**********************************************************************
 * 1) 🔧  Generic helpers & layout components                         *
 **********************************************************************/
const SectionTitle = ({ children }) => (
  <h2 className="text-lg font-semibold mb-4">{children}</h2>
);

const CardWrapper = ({ children, className = "" }) => (
  <Card className={`p-4 ${className}`}>
    <CardContent>{children}</CardContent>
  </Card>
);

const Donut = ({ data, colors }) => (
  <ResponsiveContainer width="100%" height={200}>
    <PieChart margin={{ right: 60 }}>
      <Pie data={data} dataKey="value" innerRadius={60} outerRadius={90}>
        {data.map((_, i) => (
          <Cell key={i} fill={colors[i % colors.length]} />
        ))}
        <LabelList dataKey="value" position="inside" fill="#fff" />
      </Pie>
      <Legend layout="vertical" align="right" verticalAlign="middle" />
    </PieChart>
  </ResponsiveContainer>
);

/**********************************************************************
 * 2) 📊  Mock data                                                   *
 **********************************************************************/
// -- Dashboard -------------------------------------------------------
const kpis = [
  { label: "Total Employees", value: 23541, delta: 5, icon: Users },
  { label: "Total Projects", value: 12389, delta: -8, icon: Briefcase },
  { label: "Job Applicants", value: 17389, delta: 4, icon: ClipboardList },
  { label: "Job Views", value: 9993, delta: -3, icon: Activity },
];
const workingFormat = [
  { name: "Remote", value: 220 },
  { name: "Hybrid", value: 180 },
  { name: "On‑site", value: 120 },
];
const avgKPI = ["Jan", "Feb", "Mar", "Apr", "May", "Jun"].map((m) => ({
  month: m,
  kpi: 60 + Math.random() * 10,
}));
const schedule = [
  { title: "Interview – UX Designer", time: "09:00–10:00" },
  { title: "Retro Day – HR Dept", time: "14:00–17:00" },
];

// -- Recruitment -----------------------------------------------------
const SOURCE_COLORS = ["#a78bfa", "#6366f1", "#c4b5fd", "#8b5cf6"];
const funnelData = [
  { stage: "Applications", value: 929 },
  { stage: "Screening", value: 820 },
  { stage: "Interviews", value: 680 },
  { stage: "Offers", value: 449 },
  { stage: "Hires", value: 353 },
];
const hiringTrend = ["Jan", "Feb", "Mar", "Apr", "May"].map((m, i) => ({
  month: m,
  hires: 220 + 20 * i,
}));
const sourceSplit = [
  { name: "Job Boards", value: 40 },
  { name: "Referral", value: 30 },
  { name: "Agency", value: 20 },
  { name: "Direct", value: 10 },
];

// -- Workforce -------------------------------------------------------
const GENDER_COLORS = ["#c4b5fd", "#6366f1"];
const GENERATION_COLORS = ["#fde047", "#fbbf24", "#f59e0b", "#b45309"];
const genderStructure = [
  { name: "Female", value: 45 },
  { name: "Male", value: 55 },
];
const generationData = [
  { name: "Gen Z", value: 15 },
  { name: "Gen Y", value: 45 },
  { name: "Gen X", value: 30 },
  { name: "Boomer", value: 10 },
];
const ageDistribution = [
  { range: "20‑24", count: 400 },
  { range: "25‑29", count: 820 },
  { range: "30‑34", count: 730 },
  { range: "35‑39", count: 540 },
];

// -- Productivity ----------------------------------------------------
const prodKPI = [
  { label: "Pick UPH", val: 118, unit: "" },
  { label: "Pack UPH", val: 111, unit: "" },
  { label: "Err Rate", val: 4.2, unit: "%" },
  { label: "Cap Util", val: 82, unit: "%" },
];
const uphData = [
  { hour: "08", pick: 120, pack: 110 },
  { hour: "09", pick: 135, pack: 118 },
  { hour: "10", pick: 142, pack: 124 },
  { hour: "11", pick: 138, pack: 121 },
];
const errTrend = uphData.map((d) => ({
  hour: d.hour,
  err: 3.8 + Math.random() * 0.6,
}));
const revStaff = [
  { q: "Q1", jr: 320, mid: 450, sr: 520 },
  { q: "Q2", jr: 330, mid: 460, sr: 540 },
  { q: "Q3", jr: 340, mid: 470, sr: 560 },
];

// -- Attendance ------------------------------------------------------
const otTrend = [
  { month: "Jan", ot: 8.2 },
  { month: "Feb", ot: 8.7 },
  { month: "Mar", ot: 9.1 },
];
const absenceTrend = [
  { month: "Jan", pct: 8.5 },
  { month: "Feb", pct: 9.2 },
  { month: "Mar", pct: 10.1 },
];

// -- Diversity -------------------------------------------------------
const promoRate = [
  { gen: "Gen Z", male: 12, female: 14 },
  { gen: "Gen Y", male: 8, female: 10 },
];
const payGap = [
  { level: "Jr", male: 42, female: 40 },
  { level: "Mid", male: 62, female: 59 },
  { level: "Sr", male: 88, female: 84 },
];
const leadership = [
  { name: "Female", value: 35 },
  { name: "Male", value: 65 },
];

/**********************************************************************
 * 3) 🧩  Dashboard widgets                                           *
 **********************************************************************/
const KPIGrid = () => (
  <div className="grid grid-cols-2 md:grid-cols-4 gap-4">
    {kpis.map(({ label, value, delta, icon: Icon }) => (
      <CardWrapper key={label} className="border">
        <div className="flex items-center justify-between text-xs text-slate-500">
          {label}
          <Icon size={14} />
        </div>
        <div className="text-2xl font-bold text-indigo-700">
          {value.toLocaleString()}
        </div>
        <div className={`text-xs ${delta > 0 ? "text-emerald-600" : "text-rose-600"}`}>{
          delta > 0 ? "+" : ""
        }{delta}%</div>
      </CardWrapper>
    ))}
  </div>
);

const WorkingFormat = () => (
  <CardWrapper>
    <SectionTitle>Working Format</SectionTitle>
    <Donut data={workingFormat} colors={["#22c55e", "#3b82f6", "#a855f7"]} />
  </CardWrapper>
);

const AvgKPICard = () => (
  <CardWrapper>
    <SectionTitle>Average team KPI</SectionTitle>
    <ResponsiveContainer width="100%" height={200}>
      <BarChart data={avgKPI}>
        <XAxis dataKey="month" fontSize={10} />
        <Bar dataKey="kpi" fill="#6366f1" radius={[4, 4, 0, 0]} />
      </BarChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const ScheduleCard = () => (
  <CardWrapper>
    <SectionTitle>Schedule</SectionTitle>
    <ul className="space-y-2 text-sm">
      {schedule.map((s, i) => (
        <li key={i} className="flex justify-between">
          <span>{s.title}</span>
          <span className="text-slate-500">{s.time}</span>
        </li>
      ))}
    </ul>
  </CardWrapper>
);

const DashboardTab = () => (
  <>
    <SectionTitle>Snapshot KPIs</SectionTitle>
    <KPIGrid />

    <div className="grid grid-cols-12 gap-6 mt-6">
      <div className="col-span-12 lg:col-span-4">
        <WorkingFormat />
      </div>
      <div className="col-span-12 lg:col-span-4">
        <AvgKPICard />
      </div>
      <div className="col-span-12 lg:col-span-4">
        <ScheduleCard />
      </div>
    </div>
  </>
);
/*********************************************************
 * 4) 🛠️  Recruitment widgets
 *********************************************************/
const RecruitmentFunnel = () => (
  <CardWrapper>
    <SectionTitle>Recruitment Funnel</SectionTitle>
    <ResponsiveContainer width="100%" height={350}>
      <FunnelChart>
        <Tooltip />
        <Funnel dataKey="value" data={funnelData}>
          {funnelData.map((d, i) => (
            <Cell key={d.stage} fill={SOURCE_COLORS[i]} />
          ))}
          <LabelList dataKey="stage" position="insideStart" dy={-12} fill="#fff" />
          <LabelList dataKey="value" position="insideEnd"  dy={ 12} fill="#fff" />
        </Funnel>
      </FunnelChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const HiringTrend = () => (
  <CardWrapper>
    <SectionTitle>Monthly Hiring Trend</SectionTitle>
    <ResponsiveContainer width="100%" height={200}>
      <LineChart data={hiringTrend}>
        <XAxis dataKey="month" fontSize={10} />
        <Line dataKey="hires" stroke="#4F46E5" strokeWidth={2} dot />
        <Tooltip />
      </LineChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const SourceSplit = () => (
  <CardWrapper>
    <SectionTitle>Source Split</SectionTitle>
    <Donut data={sourceSplit} colors={SOURCE_COLORS} />
  </CardWrapper>
);

const RecruitmentTab = () => (
  <>
    <SectionTitle>Recruitment</SectionTitle>
    <div className="grid grid-cols-12 gap-6">
      <div className="col-span-12 lg:col-span-6"><RecruitmentFunnel /></div>
      <div className="col-span-12 lg:col-span-6 space-y-6">
        <HiringTrend />
        <SourceSplit />
      </div>
    </div>
  </>
);
/*********************************************************
 * 5) 👥  Workforce widgets
 *********************************************************/
const GenderPie = () => (
  <CardWrapper>
    <SectionTitle>Gender Structure</SectionTitle>
    <Donut data={genderStructure} colors={GENDER_COLORS} />
  </CardWrapper>
);

const GenerationPie = () => (
  <CardWrapper>
    <SectionTitle>Generation Split</SectionTitle>
    <Donut data={generationData} colors={GENERATION_COLORS} />
  </CardWrapper>
);

const AgeHist = () => (
  <CardWrapper>
    <SectionTitle>Age Distribution</SectionTitle>
    <ResponsiveContainer width="100%" height={200}>
      <BarChart data={ageDistribution} layout="vertical" margin={{ left: 48 }}>
        <YAxis dataKey="range" type="category" width={60} fontSize={10} />
        <XAxis type="number" hide />
        <Bar dataKey="count" fill="#8B5CF6" />
      </BarChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const WorkforceTab = () => (
  <>
    <SectionTitle>Workforce</SectionTitle>
    <div className="grid grid-cols-12 gap-6">
      <div className="col-span-12 lg:col-span-4"><GenderPie /></div>
      <div className="col-span-12 lg:col-span-4"><GenerationPie /></div>
      <div className="col-span-12 lg:col-span-4"><AgeHist /></div>
    </div>
  </>
);

/*********************************************************
 * 6) 🚀  Productivity widgets
 *********************************************************/
const KPIGridSmall = () => (
  <div className="grid grid-cols-2 md:grid-cols-4 gap-4">
    {prodKPI.map(k => (
      <CardWrapper key={k.label} className="border">
        <div className="text-xs text-slate-500">{k.label}</div>
        <div className="text-xl font-bold text-indigo-700">
          {k.val}{k.unit}
        </div>
      </CardWrapper>
    ))}
  </div>
);

const UPHLineChart = () => (
  <CardWrapper>
    <SectionTitle>Pick vs Pack UPH (last 4 hrs)</SectionTitle>
    <ResponsiveContainer width="100%" height={200}>
      <LineChart data={uphData}>
        <XAxis dataKey="hour" fontSize={10} />
        <Line dataKey="pick" stroke="#4F46E5" dot name="Pick" />
        <Line dataKey="pack" stroke="#A78BFA" dot name="Pack" />
        <Tooltip />
        <Legend verticalAlign="middle" align="right" layout="vertical" />
      </LineChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const ErrorAreaChart = () => (
  <CardWrapper>
    <SectionTitle>Error Rate %</SectionTitle>
    <ResponsiveContainer width="100%" height={180}>
      <AreaChart data={errTrend}>
        <XAxis dataKey="hour" fontSize={10} />
        <Area dataKey="err" stroke="#EF4444" fill="#FECACA" name="Err %" />
        <Tooltip formatter={(v) => `${v.toFixed(1)}%`} />
      </AreaChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const RevenueStack = () => (
  <CardWrapper>
    <SectionTitle>Revenue per Staff (k$)</SectionTitle>
    <ResponsiveContainer width="100%" height={220}>
      <BarChart data={revStaff}>
        <XAxis dataKey="q" fontSize={10} />
        {["jr","mid","sr"].map((k,i)=>(
          <Bar key={k} dataKey={k} stackId="rev"
               fill={["#c4b5fd","#a78bfa","#6366f1"][i]}
               name={["Junior","Mid","Senior"][i]}>
            {k==="sr" && <LabelList dataKey="sr" position="top" />}
          </Bar>
        ))}
        <Legend layout="vertical" align="right" verticalAlign="middle"/>
      </BarChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const ProductivityTab = () => (
  <>
    <SectionTitle>Productivity</SectionTitle>
    <KPIGridSmall />
    <div className="grid grid-cols-12 gap-6 mt-6">
      <div className="col-span-12 lg:col-span-6"><UPHLineChart /></div>
      <div className="col-span-12 lg:col-span-6 space-y-6">
        <ErrorAreaChart />
        <RevenueStack />
      </div>
    </div>
  </>
);
/*********************************************************
 * 7) 🕒  Attendance widgets
 *********************************************************/
const AbsenceArea = () => (
  <CardWrapper>
    <SectionTitle>Absence Trend %</SectionTitle>
    <ResponsiveContainer width="100%" height={200}>
      <AreaChart data={absenceTrend}>
        <XAxis dataKey="month" fontSize={10} />
        <Area dataKey="pct" stroke="#EF4444" fill="#fecaca" />
        <Tooltip formatter={(v)=>`${v}%`} />
      </AreaChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const OTBar = () => (
  <CardWrapper>
    <SectionTitle>Monthly OT hours</SectionTitle>
    <ResponsiveContainer width="100%" height={160}>
      <BarChart data={otTrend}>
        <XAxis dataKey="month" fontSize={10} />
        <Bar dataKey="ot" fill="#f59e0b">
          <LabelList dataKey="ot" position="top" />
        </Bar>
      </BarChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const AttendanceTab = () => (
  <>
    <SectionTitle>Attendance</SectionTitle>
    <div className="grid grid-cols-12 gap-6">
      <div className="col-span-12 lg:col-span-6"><AbsenceArea/></div>
      <div className="col-span-12 lg:col-span-6"><OTBar/></div>
    </div>
  </>
);

/*********************************************************
 * 8) 🌈  Diversity widgets
 *********************************************************/
const LeadershipDonut = () => (
  <CardWrapper>
    <SectionTitle>Leadership Diversity</SectionTitle>
    <Donut data={leadership} colors={["#c4b5fd","#6366f1"]}/>
  </CardWrapper>
);

const PromotionStack = () => (
  <CardWrapper>
    <SectionTitle>Promotion Rate %</SectionTitle>
    <ResponsiveContainer width="100%" height={200}>
      <BarChart data={promoRate}>
        <XAxis dataKey="gen" fontSize={10}/>
        <Bar dataKey="male"   stackId="p" fill="#6366f1" name="Male"/>
        <Bar dataKey="female" stackId="p" fill="#c4b5fd" name="Female"/>
        <Legend/>
        <Tooltip formatter={(v)=>`${v}%`}/>
      </BarChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const PayGapBar = () => (
  <CardWrapper>
    <SectionTitle>Pay Gap (k$)</SectionTitle>
    <ResponsiveContainer width="100%" height={200}>
      <BarChart data={payGap}>
        <XAxis dataKey="level" fontSize={10}/>
        <Bar dataKey="male"   fill="#6366f1" name="Male"/>
        <Bar dataKey="female" fill="#c4b5fd" name="Female"/>
        <Legend/>
        <Tooltip formatter={(v)=>`$${v}k`}/>
      </BarChart>
    </ResponsiveContainer>
  </CardWrapper>
);

const DiversityTab = () => (
  <>
    <SectionTitle>Diversity</SectionTitle>
    <div className="grid grid-cols-12 gap-6">
      <div className="col-span-12 lg:col-span-6 space-y-6">
        <LeadershipDonut/>
        <PromotionStack/>
      </div>
      <div className="col-span-12 lg:col-span-6"><PayGapBar/></div>
    </div>
  </>
);

/*********************************************************
 * 9) 🗂️  Navigation & root scaffold
 *********************************************************/
const NAV = [
  { key:"dashboard",    icon:<Home size={18}/> },
  { key:"recruitment",  icon:<Activity size={18}/> },
  { key:"workforce",    icon:<Users size={18}/> },
  { key:"productivity", icon:<Briefcase size={18}/> },
  { key:"attendance",   icon:<Calendar size={18}/> },
  { key:"diversity",    icon:<CheckCircle size={18}/> },
];

const Sidebar = ({ tab, setTab }) => (
  <aside className="hidden lg:flex flex-col gap-6 px-4 py-6 bg-white/80 border-r w-16">
    {NAV.map(({key,icon})=>(
      <button key={key}
              onClick={()=>setTab(key)}
              className={tab===key ? "text-indigo-600" : "text-slate-500"}>
        {icon}
      </button>
    ))}
  </aside>
);

export default function HRDashboard() {
  const [tab,setTab] = useState<keyof typeof NAV[number]["key"]>("dashboard");

  return (
    <div className="h-screen flex bg-indigo-50/40">
      <Sidebar tab={tab} setTab={setTab}/>

      <div className="flex-1 flex flex-col overflow-hidden">
        {/* Header */}
        <header className="flex items-center justify-between px-6 py-3 border-b bg-white/80 backdrop-blur">
          <h1 className="text-xl font-semibold">Fulfillment HR Dashboard</h1>
          <Bell size={18} className="text-slate-500"/>
        </header>

        {/* Main content */}
        <main className="flex-1 overflow-y-auto p-6 space-y-10">
          {tab==="dashboard"   && <DashboardTab/>}
          {tab==="recruitment" && <RecruitmentTab/>}
          {tab==="workforce"   && <WorkforceTab/>}
          {tab==="productivity"&& <ProductivityTab/>}
          {tab==="attendance"  && <AttendanceTab/>}
          {tab==="diversity"   && <DiversityTab/>}
        </main>
      </div>
    </div>
  );
}
